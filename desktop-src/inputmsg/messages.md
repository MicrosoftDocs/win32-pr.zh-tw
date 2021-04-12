---
title: 訊息
description: 本節中的主題提供特定指標輸入訊息和通知的參考規格。
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3e143990c65daad306ef6f743d25ef4e0cca8001
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375277"
---
# <a name="messages"></a>訊息

本節中的主題提供特定 [指標輸入訊息和通知](messages-and-notifications-portal.md)的參考規格。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md) <br/></td>
<td>傳送至視窗時，在第一次偵測到指標輸入時，為了判斷 [直接操作](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)最可能的輸入目標。 <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md) <br/></td>
<td>當指標在視窗的非工作區上進行聯繫時公佈。 訊息會以指標所要接觸的視窗為目標。 指標會隱含地捕捉至視窗，讓視窗繼續接收指標的輸入，直到它中斷 contact 為止。 <br/> 如果視窗已捕捉到此指標，則不會張貼此訊息。 相反地，[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) 會張貼至已捕捉到此指標的視窗。 <br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md) <br/></td>
<td>在視窗的非工作區上建立連絡人的指標中斷連絡人時張貼。 這則訊息會以視窗為目標，指標會在該視窗上變成連絡人，而指標會在該時間點以隱含方式捕捉至視窗，讓視窗繼續接收指標的輸入，直到中斷連絡人為止，包括 [<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md) 通知。 <br/> 如果視窗已捕捉到此指標，則不會張貼此訊息。 相反地，[<strong>WM_POINTERUP</strong>] (wm-pointerup.md) 會張貼至已捕捉到此指標的視窗。 <br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md) <br/></td>
<td>張貼以提供指標的更新，以在視窗的非工作區上建立連絡人，或是當滑鼠停留 uncaptured 連絡人在視窗的非工作區上移動時。 當指標停留時，訊息會以指標發生的任何視窗為目標。 當指標與介面聯繫時，指標就會隱含地捕捉到指標所變成的視窗，而該視窗會繼續接收指標的輸入，直到中斷連絡人為止。 <br/> 如果視窗已捕捉到此指標，則不會張貼此訊息。 相反地，[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md) 會張貼至已捕捉到此指標的視窗。<br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md) <br/></td>
<td>當子系視窗發生重大動作時，傳送至視窗。 此訊息現在已擴充為包含 [<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) 事件。 建立子視窗時，系統會在建立視窗的 [<strong>CreateWindow</strong>] (/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [<strong>CreateWindowEx</strong>] (/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式之前，傳送 [<strong>WM_PARENTNOTIFY</strong>] (/previous-versions/windows/desktop/inputmsg/wm-parentnotify) 。 當子視窗被終結時，系統會先傳送訊息，然後再進行任何損毀視窗的處理。<br/> 視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。 <br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTI加值稅E</strong>] (wm-pointeractivate.md) <br/></td>
<td>當主要指標在視窗上產生 [<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) 時，傳送至非使用中的視窗。 只要訊息保持未處理狀態，它就會向上移動父視窗鏈，直到到達最上層視窗為止。 應用程式可以回應此訊息，以指定是否要啟用它們。<br/> 視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。 <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md) <br/></td>
<td>傳送至遺失輸入指標之捕捉的視窗。<br/> 視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md) <br/></td>
<td>當已連接數位板的監視器設定有變更時，傳送至視窗。 此訊息包含顯示模式調整的相關資訊。 <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md) <br/></td>
<td>在輸入數位板的範圍內偵測到指標裝置時，傳送至視窗。 此訊息包含裝置及其鄰近性的相關資訊。 <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md) <br/></td>
<td>當指標裝置已決策與輸入數位板的範圍時，傳送至視窗。 此訊息包含裝置及其鄰近性的相關資訊。 <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md) <br/></td>
<td>當指標在視窗的工作區上進行接觸時張貼。 此輸入訊息會以指標所用的視窗為目標，並以隱含方式將指標捕捉至視窗，讓視窗繼續接收指標的輸入，直到中斷連絡人為止。 <br/> 視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。<br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md) <br/></td>
<td>當新指標在視窗上進入偵測範圍時傳送至視窗 (停留) ，或當現有指標在視窗界限內移動時。 <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md) <br/></td>
<td>當指標在視窗上離開偵測範圍時傳送至視窗 (停留) 或指標移至視窗界限之外。 <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md) <br/></td>
<td>當指標輸入路由傳送至另一個進程時，在接收輸入的進程上發生。<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md) <br/></td>
<td>傳送至所有進程， (透過 [<strong>AddContentWithCrossProcessChaining</strong>] 設定跨進程連結的所有進程 (/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) ，且目前的進程在收到 [<strong>WM_POINTERUP</strong>] (wm-pointerup.md) 訊息時，不會處理指標輸入) 與特定指標識別碼相關聯。 <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md) <br/></td>
<td>在進行中指標輸入時傳送，針對現有的指標識別碼，會在針對跨進程連結 ( [<strong>AddContentWithCrossProcessChaining</strong>] (/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) ) 的內容之間，從一個進程轉換成另一個進程。<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md) <br/></td>
<td>當在視窗的工作區上建立連絡人的指標中斷連絡人時張貼。 此輸入訊息的目標視窗是指標所用的視窗，而指標會在該視窗上以隱含方式捕捉至視窗，讓視窗繼續接收輸入訊息，包括 [<strong>WM_POINTERUP</strong>] (wm-pointerup.md) 指標的通知，直到中斷連絡人為止。 <br/> 視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。 <br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md) <br/></td>
<td>張貼以提供指標的更新，而該指標是在視窗的工作區上，或是在視窗的工作區上停留在滑鼠停留 uncaptured 指標上。 當指標停留時，訊息會以指標發生的任何視窗為目標。 當指標與介面聯繫時，指標就會隱含地捕捉到指標所變成的視窗，而該視窗會繼續接收指標的輸入，直到中斷連絡人為止。 <br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md) <br/></td>
<td>當滾動滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。 <br/> 視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。<br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md) <br/></td>
<td>當水準滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。 <br/> 視窗會透過其 [<strong>WindowProc</strong>] (/previous-versions/windows/desktop/legacy/ms633573 (v = 與 85) ) 函式接收此訊息。<br/>
<blockquote>
[!Important]<br />
桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md) <br/></td>
<td>傳送至觸控下的視窗，以便判斷最可能的觸控目標。 <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指標輸入訊息參考](wmpointer-reference.md)
</dt> </dl>

 

