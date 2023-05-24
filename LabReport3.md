# Cse 15L Lab Report 3

## Researching Commands - Grep 
For my lab report, I focused on the grep command.
A shortcut I found useful for finding different command line options for grep was using the

         man grep
         
command. This command prompted various possible command line options I could use.

<img src = "https://raw.githubusercontent.com/deliasi/LabReport3/main/Screen%20Shot%202023-05-09%20at%205.34.46%20PM.png">

### First Command Line Option (Grep -A/-B)
This command allows us to display as many lines before or after our input matches. In this case,
'wait' is within 'waiting', which still prints the output below.

Using -A:

      DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -A 5 "wait" 5_Legal_Groups.txt
      client waiting room. The building is close in, across the street
      from West High and two blocks from the Gateway. It has its own
      parking, something that's hard to find downtown and which has been
      a problem for staff as well as clients. Owning and sharing the
      building and not paying rent times five will save the non-profit
      agencies about $375,000 each year. My assistant, Charity
      DERRICKS-MacBook-Air:media alenooshhambarchian$ 

In this example, we see 5 lines displayed after the line in which our key word is matched.
    
-B:

        DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -B 5 "wait" 5_Legal_Groups.txt
        the Multi-Cultural Legal Center, the Senior Lawyer Volunteer
        Project and Utah Legal Services will share the new facility, and
        last Wednesday their board members were given a tour of the
        Community Legal Center hosted by staff members of the five
        agencies. All of the agencies can share the same reception area and
        client waiting room. The building is close in, across the street
        DERRICKS-MacBook-Air:media alenooshhambarchian$ 

In this example, we see 5 lines displayed before the line in which our key word is matched.

### Second Command Line Option (Grep -c)
This command allows us to find the occurrences of patterns in our text files. A number is printed out
when this command is run.

         DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -c 'say' Farm_workers.txt
         2

In this example, two lines contain our desired word, "say", and therefore, 2 is printed as our ouput.

         DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -c 'finally' Farm_workers.txt
         0
         DERRICKS-MacBook-Air:media alenooshhambarchian$ 
        
In this example, no lines contain our desired word, "finally", and therefore, 0 is printed as our ouput.


### Third Command Line Option (Grep -o)
This command prints the amount of matching parts to the input. Only the input is printed in the output
and not words around. The input is outputted as many times as it shows up within the text.

        DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -o "say"  Ginny_Kilgore.txt
        say
        say
        
In this example. "say" is found two times within the text and therefore is printed two times in the output.

        DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -o "to" Ginny_Kilgore.txt
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        to
        DERRICKS-MacBook-Air:media alenooshhambarchian$ 

In this example. "to" is found 17 times within the text and therefore is printed 17 times in the output.

### Fourth Command Line Option (Grep -w)
This command helps us find the amount of times a whole word is found within the text. For example,
if we choose "say", and the text contains "saying", it will not print that line.

        DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -w 'to' Pro_Bono_Services.txt
        Marketing Group to Offer 'Pro Bono' Services
        A legal marketing group in Chicago is asking its members to do
        offer pro bono services to legal-aid organizations in the city.
        While gaining access to justice is their first priority, most
        resources to develop marketing.
        professionals within the law firms to do some of the same [pro bono
        work] we ask our lawyers to do," said Michael R. Ralston, president
        that recognition that led us to ... undertake this."
        Although it's common for lawyers to offer pro bono services to
        "We thought it was a great opportunity for legal marketers to
        give something back to the legal community," she said.
        organizations, will hold a seminar/reception with LMA members to
        To start, the Foundation hopes to match LMA members with at
        said the groups provide little information to the general public
        But the legal-aid groups don't know how to spread the word about
        "Bottom line -- we just don't know how to do that," Corbett
        position is the first in CCR's history and was developed to expand
        "It's very new to the organization and it's interesting coming
        One reason, she said, is a due to a limited budget.
        said. "This is really going to push us forward."

In this example, "to" is found many times within our text and, therefore, we see many lines printed in our ouput that each contain "to".

        DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -w 'out' Pro_Bono_Services.txt
        DERRICKS-MacBook-Air:media alenooshhambarchian$ grep -w 'on' Pro_Bono_Services.txt
        legal-aid organizations put marketing and development on the back
        They often survive on a bare-bones budget, a staff of volunteers
        DERRICKS-MacBook-Air:media alenooshhambarchian$
        
In this example, "on" is found twice  within our text and, therefore, we see two lines printed in our ouput that also contain "on".
As we see in our terminal, if no word withtin the text matches our input, no ouput will be printed.
