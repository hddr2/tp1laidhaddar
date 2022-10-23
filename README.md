# tp1laidhaddar

import operator


def calc_occ(text2):
    global v
    text2.replace(" ", "")
    count_a = 0
    count_b = 0
    count_c = 0
    count_d = 0
    count_e = 0
    count_f = 0
    count_g = 0
    count_h = 0
    count_i = 0
    count_j = 0
    count_k = 0
    count_l = 0
    count_m = 0
    count_n = 0
    count_o = 0
    count_p = 0
    count_q = 0
    count_r = 0
    count_s = 0
    count_t = 0
    count_u = 0
    count_v = 0
    count_w = 0
    count_x = 0
    count_y = 0
    count_z = 0
    freq_dict = {'a': count_a, 'b': count_b, 'c': count_c, 'd': count_d, 'e': count_e, 'f': count_f, 'g': count_g,
                 'h': count_h, 'i': count_i, 'j': count_j, 'k': count_k, 'l': count_l, 'm': count_m, 'n': count_n,
                 'o': count_o, 'p': count_p, 'q': count_q, 'r': count_r, 's': count_s, 't': count_t, 'u': count_u,
                 'v': count_v, 'w': count_w, 'x': count_x, 'y': count_y, 'z': count_z}
    alph = ['e', 'a', 'i', 's', 't', 'n', 'r', 'u', 'l', 'o', 'd', 'm', 'p', 'c', 'v',
            'q', 'f', 'g', 'b', 'j', 'h', 'x', 'z', 'y', 'w', 'k']
    for letter in text2:
        if letter == 'a':
            count_a = count_a + 1
            freq_dict['a'] = count_a
        elif letter == 'b':
            count_b += 1
            freq_dict['b'] = count_b
        elif letter == 'c':
            count_c += 1
            freq_dict['c'] = count_c
        elif letter == 'd':
            count_d += 1
            freq_dict['d'] = count_d
        elif letter == 'e':
            count_e += 1
            freq_dict['e'] = count_e
        elif letter == 'f':
            count_f += 1
            freq_dict['f'] = count_f
        elif letter == 'g':
            count_g += 1
            freq_dict['g'] = count_g
        elif letter == 'h':
            count_h += 1
            freq_dict['h'] = count_h
        elif letter == 'i':
            count_i += 1
            freq_dict['i'] = count_i
        elif letter == 'j':
            count_j += 1
            freq_dict['j'] = count_j
        elif letter == 'k':
            count_k += 1
            freq_dict['k'] = count_k
        elif letter == 'l':
            count_l += 1
            freq_dict['l'] = count_l
        elif letter == 'm':
            count_m += 1
            freq_dict['m'] = count_m
        elif letter == 'n':
            count_n += 1
            freq_dict['n'] = count_n
        elif letter == 'o':
            count_o += 1
            freq_dict['o'] = count_o
        elif letter == 'p':
            count_p += 1
            freq_dict['p'] = count_p
        elif letter == 'q':
            count_q += 1
            freq_dict['q'] = count_q
        elif letter == 'r':
            count_r += 1
            freq_dict['r'] = count_r
        elif letter == 's':
            count_s += 1
            freq_dict['s'] = count_s
        elif letter == 't':
            count_t += 1
            freq_dict['t'] = count_t
        elif letter == 'u':
            count_u += 1
            freq_dict['u'] = count_u
        elif letter == 'v':
            count_v += 1
            freq_dict['v'] = count_v
        elif letter == 'w':
            count_w += 1
            freq_dict['w'] = count_w
        elif letter == 'x':
            count_x += 1
            freq_dict['x'] = count_x
        elif letter == 'y':
            count_y += 1
            freq_dict['y'] = count_y
        elif letter == 'z':
            count_z += 1
            freq_dict['z'] = count_z
    sorted_dict = {}
    # tri de dictionnaire qui contient les lettres et ses fréquences
    sorted_dict = sorted(freq_dict.items(), key=operator.itemgetter(1), reverse=True)
    for key,value in sorted_dict:
        print(f"{key} => {value}")
    # récupérer la lettre la plus fréquente dans le message codé
    freq_letter = max(freq_dict, key=freq_dict.get)
    # supposer que la lettre la plus fréquente que c'est un e
    k = ord(freq_letter) - ord(alph[0])

    for char in text2:
        # récupérer le code ASCII de la lettre a(début de l'alphabet)
        begin = ord('a')
        # char
        char = chr((ord(char) - begin - k) % 26 + begin)
        v = "".join(char)
        print(v, end='')


text_chiff = "Uj lahycxpajyqrn zdjwcrzdn ynavnc un lqrooanvnwc bnldarbn nc un cajwbonac mn cxdb chynb m’rwoxavjcrxwb" \
             " j u’jrmn mn lunb zdjwcrzdnb dcrurbjwc unb yaxyarncnb" "  yjacrldurnanb mn uj vnljwrzdn mnb jcxvnb" \
             "uj lun mn lqrooanvnwc nbc yjacjpnn dwrzdnvnwc yja u’ngynmrcnda nc un mnbcrwjcjran " \
             "Br nuun nbc rwcnalnycnn yja dw crnab" "  nuun mnernwc jdcxvjcrzdnvnwc rwejurmn nc unb rwoxavjcrxwb zd’nuun yaxcnpn" \
             " mnernwwnwc raanenabrkunvnwc ruurbrkunb" " Cxbqrkj ernwc dwn wxdenuun oxrb mn mnvxwcana un yxcnwcrnu mn uj cnlqwxuxprn " \
             "nc bxw jejwln mjwb ln mxvjrwn nw yanbnwcjwc" \
             "un mrbyxbrcro mn mrbcarkdcrxw mn lunb zdjwcrzdnb un yudb ajyrmn jd vxwmn"   \
            


calc_occ(text_chiff)
