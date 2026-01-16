import os
import string
import random 

c:list='!"#$%&()*+,-./:;<=>?@[]^_`{|}~'
a=list(string.ascii_letters+string.digits+c)
a2=a.copy()
random.shuffle(a2)
a3=a.copy()
random.shuffle(a3)
a4=a.copy()
random.shuffle(a4) 

os.system('cls')

#for n,i in enumerate(a):
#    print(f"'{i}':'{a[n]+a2[n]+a3[n]+a4[n]}'",end=',\n')
chars=dict({'a':'a:7W',
'b':'bwrk','c':'ckRp',
'd':'ds*+','e':'e;Kg',
'f':'fq->','g':'gZ{f',
'h':'h&fo','i':'i9e?',
'j':'j^&9','k':'kC,|',
'l':'l(hq','m':'m@4F',
'n':'nyDl','o':'oe2;',
'p':'p1`*','q':'qKk(',
'r':'r/ET','s':'sEOR',
't':'tJ>s','u':'u>CI',
'v':'v{bK','w':'wn]h',
'x':'x"X6','y':'y0#j',
'z':'z|$&','A':'AU;^',
'B':'Bb/<','C':'C?6a',
'D':'D3I3','E':'E7G,',
'F':'F~cd','G':'G,|J',
'H':'H4me','I':'I`vb',
'J':'Jz!8','K':'KRNz',
'L':'Lf9G','M':'M5St',
'N':'Nug!','O':'O8?V',
'P':'PxVA','Q':'Q$H)',
'R':'RpM.','S':'Sauv',
'T':'T=oy','U':'UX8M',
'V':'V}zC','W':'Wd%w',
'X':'X<.S','Y':'YHUD',
'Z':'Zl^`','0':'0MFr',
'1':'1vBU','2':'2In}',
'3':'3%Px','4':'4TAQ',
'5':'5gQn','6':'6)57',
'7':'7-_m','8':'8#x%',
'9':'9N1{','!':'!Ql0',
'"':'"A)E','#':'#O0N',
'$':'$Yiu','%':'%2JX',
'&':'&[tB','(':'(BaY',
')':')jyc','*':'*GqH',
'+':'+tZL',',':',o<4',
'-':'-!s#','.':'.."P',
'/':'/]+1',':':':*=-',
';':';m(_','<':'<V3i',
'=':'=+YZ','>':'>PL2',
'?':'?iW@','@':'@_T:',
'[':'[rw"',']':']W@]',
'^':'^Ld5','_':'_6:O',
'`':'`S[$','{':'{h~~',
'|':'|cp/','}':'}F}=',
'~':'~Dj[',' ':'g6js',
'\\':'fu&;',"'":'a)8q'})


#for g,s in chars.items():
#    print(f"'{s}':'{g}'",end=',\n')

r_chars=dict({'a:7W':'a','bwrk':'b',
'ckRp':'c','ds*+':'d',
'e;Kg':'e','fq->':'f',
'gZ{f':'g','h&fo':'h',
'i9e?':'i','j^&9':'j',
'kC,|':'k','l(hq':'l',
'm@4F':'m','nyDl':'n',
'oe2;':'o','p1`*':'p',
'qKk(':'q','r/ET':'r',
'sEOR':'s','tJ>s':'t',
'u>CI':'u','v{bK':'v',
'wn]h':'w','x"X6':'x',
'y0#j':'y','z|$&':'z',
'AU;^':'A','Bb/<':'B',
'C?6a':'C','D3I3':'D',
'E7G,':'E','F~cd':'F',
'G,|J':'G','H4me':'H',
'I`vb':'I','Jz!8':'J',
'KRNz':'K','Lf9G':'L',
'M5St':'M','Nug!':'N',
'O8?V':'O','PxVA':'P',
'Q$H)':'Q','RpM.':'R',
'Sauv':'S','T=oy':'T',
'UX8M':'U','V}zC':'V',
'Wd%w':'W','X<.S':'X',
'YHUD':'Y','Zl^`':'Z',
'0MFr':'0','1vBU':'1',
'2In}':'2','3%Px':'3',
'4TAQ':'4','5gQn':'5',
'6)57':'6','7-_m':'7',
'8#x%':'8','9N1{':'9',
'!Ql0':'!','"A)E':'"',
'#O0N':'#','$Yiu':'$',
'%2JX':'%','&[tB':'&',
'(BaY':'(',')jyc':')',
'*GqH':'*','+tZL':'+',
',o<4':',','-!s#':'-',
'.."P':'.','/]+1':'/',
':*=-':':',';m(_':';',
'<V3i':'<','=+YZ':'=',
'>PL2':'>','?iW@':'?',
'@_T:':'@','[rw"':'[',
']W@]':']','^Ld5':'^',
'_6:O':'_','`S[$':'`',
'{h~~':'{','|cp/':'|',
'}F}=':'}','~Dj[':'~',
'g6js':' ','fu&;':'\\',
'a)8q':"'"})


def encrypt (sentence,chars):
    result=''
    for k in sentence:
        if k not in chars.keys():
            print(f'{k} is an invald char')
        result+=chars.get(k)
    return result

def decrypt(e_sentence,r_chars):
    c_result = ''
    for i in range(0,len(e_sentence),4):
        ch=e_sentence[i:i+4]
        c_result+=r_chars.get(ch)
    return c_result

#for i,n in chars.items():
#    for k,m in r_chars.items():
#        if i==m and n==k :
#            print(f'{i} --dicts are reversed!')

fo=input('enter a for encrypt ,or d for decrypt:  ')
while 10>0:
       
       if fo=='a':
           cs=input('enter ur sentence to be encrypted :  ').strip()
           if 'C:\\' in cs :
            indx=cs.index('C:\\')
            cs=cs[:indx]
           elif "'" in cs :
             md="'"
             md.replace("'","\'")
           print('-----------------------------ENCRYPTED-SENTENCE-----------------------------\n'
                ,encrypt(cs,chars)+'\n'
                ,'------------------------------------END------------------------------------')
           break
    
       elif fo=='d':
           ds=input('enter ur sentence to be decrypted :  ').strip()
           if 'C:\\' in ds :
             indx=fo.index('C:\\')
             fo =fo[:indx]
           elif "'" in ds :
              md="'"
              md.replace("'","\'")
           print('-----------------------------DECRYPTED-SENTENCE-----------------------------\n'
                ,decrypt(ds,r_chars),'\n'
                ,'------------------------------------END------------------------------------')
           break
       else:
          fo=input('plz choose a/d :  ')
