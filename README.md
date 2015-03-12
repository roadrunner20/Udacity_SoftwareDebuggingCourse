# Udacity_SoftwareDebuggingCourse
def stripHTMLMarkup(html):
    tag = False
    out = ""
    for c in html:
        if c is '<' and not tag: 
            tag =True
            continue #dont touch the output when changing states
        elif c is '>' and tag : 
            tag = False
            continue #dont touch the output when changing states
        if not tag : # print to the output only when in the non-tag state
           out = out + c

    return out

print stripHTMLMarkup('<b>"We Live in the World of Chaos!"</b>')
