<p style="text-align: center;">������������ ����������� ���������� ��������</p>
<p style="text-align: center;">���������� �����������</p>
<p style="text-align: center;">���������� ��������������� ����������� �����������</p>
<p style="text-align: center;">������� ���</p>
<div style="margin-bottom: 10em;"></div>
<p style="text-align: center;">������������ ������ �2</p>
<p style="text-align: center;">�� ���������� ���������� ����������������</p>
<p style="text-align: center;">����: ��������� ��������� � ����������� ���������������� ����������� � �� Windows�</p>
<div style="margin-bottom: 10em;"></div>
<p style="text-align: right;">��������:</p>
<p style="text-align: right;">������� 3 �����</p>
<p style="text-align: right;">������ ��-8</p>
<p style="text-align: right;">������� �. �.</p>
<p style="text-align: right;">��������:</p>
<p style="text-align: right;">�������� �. �.</p>
<div style="margin-bottom: 10em;"></div>
<p style="text-align: center;">����� 2023</p>

---
## ���� ������ ##
��������� ��������� ���������� ���������� � ����������� ���������������� ����������� � �� Windows.
## ������� �16 (4) ##
������� ���������� � ������� � ����� ��� ����� ������. �� ������� �� ������ ���������, ������ �� ������������ ���������� �����.
## ����������/��� ������ ##
���������� ������������ ������ � ���������� ����:
```C++
HWND BUTTON;
HWND EDIT;
```
��������� ������ � ���������� ����:
```C++
 BUTTON = CreateWindowW(TEXT("button"), TEXT("Check your guess"),
                WS_VISIBLE | WS_CHILD,
                30, 40, 200, 50,
                hWnd, (HMENU)1, NULL, NULL);

 EDIT = CreateWindowW(TEXT("edit"), TEXT("Enter number from 1 to 10"),
                WS_VISIBLE | WS_CHILD,
                400, 40, 200, 50,
                hWnd, (HMENU)2, NULL, NULL);
```
��������� ������� �� ������, ���������� ������ � ��������, ������ �� ������������:
```C++
 TCHAR buffer[256];
 GetWindowText(EDIT, buffer, 256);

 TCHAR myNumber[] = _T("7");

 if (lstrcmp(buffer, myNumber) == 0)
 {
     MessageBox(hWnd, _T("You won! My number was 7 as well"), _T("Lucky! :)"), MB_OK);
 }
 else
 {
     MessageBox(hWnd, _T("You lose! Try again"), _T("Unlucky! :("), MB_OK);
 }
```

---

������ ������:

![Main window](images/�������1.png "Main window") 

![Win dialog](images/�������2.png "Success dialog") 

![Lose dialog](images/�������3.png "Lose dialog") 