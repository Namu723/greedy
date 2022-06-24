#쳬육복

def solution(n, lost, reserve):
    _reserve = [r for r in reserve if r not in lost]
    print(_reserve)
    _lost = [l for l in lost if l not in reserve]
    print(_lost)
    for r in _reserve:
        f = r - 1
        b = r + 1
        if f in _lost:
            _lost.remove(f)
        elif b in _lost:
            _lost.remove(b)
    return n - len(_lost)


print(solution(5, [2, 4], [1, 3, 5]))
