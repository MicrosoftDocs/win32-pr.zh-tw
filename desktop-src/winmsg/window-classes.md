---
description: 本主題說明視窗類別的類型、系統如何找出它們，以及定義屬於這些類別之 windows 預設行為的元素。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: '視窗類別 (視窗和訊息) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da95fc54a9527bade0d925c1f993cf853b0ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001429"
---
# <a name="window-classes-windows-and-messages"></a>視窗類別 (視窗和訊息) 

本主題說明視窗類別的類型、系統如何找出它們，以及定義屬於這些類別之 windows 預設行為的元素。

視窗類別是一組屬性，可供系統用來作為建立視窗的範本。 每個視窗都是視窗類別的成員。 所有視窗類別都是進程特定的。

### <a name="in-this-section"></a>本節內容



| Name                                                 | 描述                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於視窗類別](about-window-classes.md)     | 討論視窗類別。 每個視窗類別都有一個相關聯的視窗程式，由相同類別的所有視窗共用。 視窗程式會處理該類別的所有視窗的訊息，因此會控制其行為和外觀。<br/> |
| [使用視窗類別](using-window-classes.md)     | 示範如何註冊本機視窗，並用它來建立主視窗。<br/>                                                                                                                                                                     |
| [視窗類別參考](window-class-reference.md) | 包含 API 參考。<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>視窗類別函數



| Name                                         | 描述                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | 抓取視窗類別的相關資訊，包括與視窗類別相關聯之小圖示的控制碼。 [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)函式不會取出小圖示的控制碼。<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | 從與指定視窗相關聯的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構中，抓取指定的32位 (**long**) 值。 <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | 從與指定視窗相關聯的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構抓取指定的值。<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | 抓取指定的視窗所屬類別的名稱。 <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | 抓取所指定視窗的相關資訊。 函式也會將指定之位移的32位 (**long**) 值抓取到額外的視窗記憶體。<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | 抓取所指定視窗的相關資訊。 函式也會將指定之位移的值抓取到額外的視窗記憶體。<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | 註冊視窗類別，以供後續使用於 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式的呼叫中。<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | 註冊視窗類別，以供後續使用於 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式的呼叫中。 <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | 針對指定之視窗所屬類別的額外類別記憶體或 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構，取代指定之位移的指定值。<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | 將指定之位移的16位 (**WORD**) 值取代為指定的視窗所屬之視窗類別的額外類別記憶體。<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | 變更指定之視窗的屬性。 函數也會將指定之位移的32位 (long) 值設定為額外的視窗記憶體。<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | 變更指定之視窗的屬性。 函數也會在額外的視窗記憶體中的指定位移上設定值。<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | 取消註冊視窗類別，釋放類別所需的記憶體。 <br/>                                                                                                                                            |



 

下列函式已過時。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a></td>
<td>抓取視窗類別的相關資訊。 <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a>函式已被<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx</strong></a>函數取代。 但是，如果您不需要類別小型圖示的相關資訊，仍然可以使用 <strong>GetClassInfo</strong>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a></td>
<td>針對指定之視窗所屬的視窗類別，將指定之位移的16位 (<strong>字</strong>) 值移入額外類別記憶體。
<blockquote>
[!Note]<br />
<em>NIndex</em>設定為 GCW_ATOM 以外的任何使用，此函式已被取代。 函式僅提供給 Windows 的16位版本相容。 應用程式應該使用 <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> 函式。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></td>
<td>將指定之位移的指定32位 (<strong>long</strong>) 值取代為指定之視窗所屬類別的額外類別記憶體或 <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> 結構。
<blockquote>
[!Note]<br />
此函數已被 <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr</strong></a> 函數取代。 若要撰寫與32位和64位版本的 Windows 相容的程式碼，請使用 <strong>SetClassLongPtr</strong>。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="window-class-structures"></a>視窗類別結構



| Name                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | 包含 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 函數所註冊的視窗類別屬性。 <br/> 此結構已由與 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)函數搭配使用的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構所取代。 如果您不需要設定與視窗類別相關聯的小圖示，仍然可以使用 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 和 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 。<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | 包含視窗類別資訊。 它會搭配 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) 和 [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  函數使用。 <br/> [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構類似于 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構。 有兩種差異。 **WNDCLASSEX** 包含 **cbSize** 成員（指定結構的大小）和 **hIconSm** 成員，其中包含與視窗類別相關聯之小圖示的控制碼。<br/> |



 

 

 
