---
title: 使用動態資料交換
description: 本主題提供有關動態資料交換的程式碼範例。
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- 動態資料交換 (DDE) 、交談
- DDE (動態資料交換) 、交談
- '資料交換、動態資料交換 (DDE) '
- 動態資料交換 (DDE) ，範例
- DDE (動態資料交換) ，範例
- 動態資料交換 (的 DDE) ，伺服器應用程式中的命令
- 伺服器應用程式中的 DDE (動態資料交換) 命令
- 動態資料交換 (DDE) 、資料連結
- DDE (動態資料交換) 、資料連結
- 動態資料交換 (DDE) 、items
- DDE (動態資料交換) 、items
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3a279e02b65d5540e5494512a44eefdfecdb18607cb12731cf7daa0d8569de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953661"
---
# <a name="using-dynamic-data-exchange"></a>使用動態資料交換

本節包含下列工作的程式碼範例：

-   [起始對話](#initiating-a-conversation)
-   [傳送單一專案](#transferring-a-single-item)
    -   [從伺服器中取出專案](#retrieving-an-item-from-the-server)
    -   [將專案提交至伺服器](#submitting-an-item-to-the-server)
-   [建立永久資料連結](#establishing-a-permanent-data-link)
    -   [起始資料連結](#initiating-a-data-link)
    -   [使用貼上連結命令起始資料連結](#initiating-a-data-link-with-the-paste-link-command)
    -   [通知用戶端資料已變更](#notifying-the-client-that-data-has-changed)
    -   [終止資料連結](#terminating-a-data-link)
-   [在伺服器應用程式中執行命令](#carrying-out-commands-in-a-server-application)
-   [終止交談](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>起始對話

若要起始動態資料交換 (DDE) 交談，用戶端會傳送 [**WM \_ DDE \_ 初始**](wm-dde-initiate.md)訊息。 通常，用戶端會呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)來廣播此訊息，並以-1 做為第一個參數。 如果應用程式已經有伺服器應用程式的視窗控制碼，它可以將訊息直接傳送到該視窗。 用戶端會藉由呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)來準備應用程式名稱和主題名稱的原子。 用戶端可以針對應用程式和主題提供 **Null** (萬用字元) 原子，要求與任何潛在的伺服器應用程式進行交談。

下列範例說明用戶端如何起始交談，同時指定了應用程式和主題。


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> 如果您的應用程式使用 **Null** 原子，則不需要使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 和 [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) 函數。 在此範例中，用戶端應用程式會建立兩個全域原子，分別包含伺服器的名稱和主題的名稱。

 

用戶端應用程式會在訊息的 *lParam* 參數中，使用這兩個原子來傳送 [**WM \_ DDE \_ 起始**](wm-dde-initiate.md)訊息。 在 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式的呼叫中，特殊的視窗控制碼（1）會指示系統將此訊息傳送給所有其他作用中的應用程式。 **SendMessage** 不會傳回用戶端應用程式，直到接收訊息的所有應用程式都將控制權傳回給系統為止。 這表示伺服器應用程式在回復中傳送的所有 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，在 **SendMessage** 呼叫傳回時，保證已由用戶端處理。

在 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 傳回之後，用戶端應用程式會刪除全域原子。

伺服器應用程式會根據下圖所示的邏輯來回應。

![伺服器應用程式回應邏輯](images/csdde-01.png)

若要認可一或多個主題，伺服器必須為每個對話建立原子 (如果有多個主題) ，並針對每個交談傳送 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，則伺服器必須有重複的應用程式名稱原子，如下列範例所示。


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



當伺服器以 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息回應時，用戶端應用程式應該將控制碼儲存至伺服器視窗。 用戶端接收控制碼做為 **WM \_ DDE \_** 通知訊息的 *wParam* 參數，然後將所有後續的 DDE 訊息傳送到此控制碼識別的伺服器視窗。

如果您的用戶端應用程式使用 **Null** atom 做為應用程式名稱或主題名稱，則預期應用程式會接收來自多個伺服器應用程式的通知。 多個通知也可以來自多個 DDE 伺服器實例，即使您的用戶端應用程式不是 **Null** ，也可以使用原子。 伺服器應該一律針對每個交談使用唯一的視窗。 用戶端應用程式中的視窗程式可以使用伺服器視窗的控制碼 (作為 [**WM \_ DDE \_ 起始**](wm-dde-initiate.md)) 的 *lParam* 參數，以追蹤多個交談。 這可讓單一用戶端視窗處理數個交談，而不需要為每個對話終止和重新連接新的用戶端視窗。

## <a name="transferring-a-single-item"></a>傳送單一專案

一旦建立了 DDE 交談之後，用戶端就可以藉由發出 [**wm \_ dde \_ 要求**](wm-dde-request.md) 訊息來從伺服器取出資料項目的值，或是藉由發出 [**wm \_ dde \_**](wm-dde-poke.md)的郵件將資料項目目值提交至伺服器。

-   [從伺服器中取出專案](#retrieving-an-item-from-the-server)
-   [將專案提交至伺服器](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>從伺服器中取出專案

若要從伺服器取出專案，用戶端會傳送一個 [**WM \_ DDE \_ 要求**](wm-dde-request.md) 訊息給伺服器，以指定要抓取的專案和格式，如下列範例所示。


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



在此範例中，用戶端會將「剪貼簿 **」格式指定為 \_ 要求** 之資料項目的慣用格式。

[**WM \_ DDE \_ 要求**](wm-dde-request.md)訊息的接收者 (server) 通常必須刪除專案 Atom，但是如果 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)呼叫失敗，用戶端就必須刪除 atom。

如果伺服器具有要求之專案的存取權，而且可以使用要求的格式來轉譯，則伺服器會將專案值複製為共用記憶體物件，並傳送 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息給用戶端，如下列範例所示。


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



在此範例中，伺服器應用程式會配置包含資料項目的記憶體物件。 資料物件會初始化為 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) 結構。

然後，伺服器應用程式會將結構的 **cfFormat** 成員設定為 CF \_ text，以通知用戶端應用程式資料是文字格式。 用戶端會將所要求資料的值複製到 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **值** 成員，以進行回應。 在伺服器填妥資料物件之後，伺服器會將資料解除鎖定，並建立包含資料項目名稱的全域 atom。

最後，伺服器會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)來發出 [**WM \_ DDE 的 \_ 資料**](wm-dde-data.md)訊息。 資料物件的控制碼和包含專案名稱的 atom 會由 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數封裝至訊息的 *lParam* 參數。

如果 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 失敗，伺服器必須使用 [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) 函式來釋放壓縮的 *lParam* 參數。 伺服器也必須釋放所接收之 [**WM \_ DDE \_ 要求**](wm-dde-request.md)訊息的封裝 *lParam* 參數。

如果伺服器無法滿足要求，它會將負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息傳送至用戶端，如下列範例所示。


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



收到 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息時，用戶端會適當地處理資料項目目值。 然後，如果在 **WM \_ dde 的 \_ 資料** 訊息中指向的 **fAckReq** 成員是1，則用戶端必須將伺服器傳送正 [**的 \_ WM \_ dde**](wm-dde-ack.md)通知訊息，如下列範例所示。


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



在此範例中，用戶端會檢查資料的格式。 如果格式不是 **CF \_ 文字** (或用戶端無法鎖定資料) 的記憶體，用戶端會傳送負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，表示它無法處理資料。 如果用戶端因為控制碼包含 **fAckReq** 成員而無法鎖定資料控制碼，則用戶端不應該傳送負 **的 \_ WM \_ DDE** 通知訊息。 相反地，用戶端應該終止交談。

如果用戶端傳送負認可以回應 [**WM \_ dde 的 \_ 資料**](wm-dde-data.md) 訊息，則伺服器會負責釋出記憶體 (但不會) *lParam* 參數，而是與負認可相關聯的 **WM \_ DDE \_ 資料** 訊息所參考的資料。

如果可以處理資料，用戶端會檢查 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **fAckReq** 成員，判斷伺服器是否要求告知用戶端已成功接收和處理資料。 如果伺服器已要求這種資訊，用戶端會傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給伺服器。

因為解除鎖定資料會使資料指標失效，所以用戶端會先儲存 **fRelease** 成員的值，再解除鎖定資料物件。 儲存值之後，用戶端會檢查它，判斷伺服器應用程式是否要求用戶端釋放包含資料的記憶體;用戶端會據以運作。

在收到負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息時，用戶端可以再次要求相同的專案值，並指定不同的剪貼簿格式。 一般而言，用戶端會先要求其可支援的最複雜格式，然後在必要時透過逐漸簡化的格式逐步執行，直到找到伺服器可以提供的格式為止。

如果伺服器支援系統主題的格式專案，用戶端可以判斷伺服器支援的剪貼簿格式，而不是在每次用戶端要求專案時進行判斷。

### <a name="submitting-an-item-to-the-server"></a>將專案提交至伺服器

用戶端可以使用 [**WM \_ DDE \_**](wm-dde-poke.md) 請求訊息，將專案值傳送至伺服器。 用戶端會呈現要傳送的專案，並傳送 **WM \_ DDE \_** 傳送訊息，如下列範例所示。


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> 使用 [**wm \_ dde \_**](wm-dde-poke.md) 訊息傳送資料時，基本上與使用 [**wm \_ dde \_ 資料**](wm-dde-data.md)傳送資料相同，不同之處在于從用戶端將 **wm \_ dde \_** 傳送至伺服器。

 

如果伺服器能夠接受用戶端所轉譯格式的資料項目目值，伺服器會適當地處理專案值，並傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給用戶端。 如果它無法處理專案值（因為其格式或基於其他原因），伺服器會傳送負的 **WM \_ DDE \_** 通知訊息給用戶端。


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



在此範例中，伺服器會呼叫 [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) ，以抓取用戶端傳送的專案名稱。 伺服器接著會判斷它是否支援該專案，以及專案是否以正確的格式轉譯 (也就是 CF \_ 文字) 。 如果專案不受支援且未以正確的格式轉譯，或伺服器無法鎖定資料的記憶體，則伺服器會將負認可傳回用戶端應用程式。 請注意，在這種情況下，傳送負認可是正確的，因為通常會假設有一組 **fAckReq** 成員設定了 [**WM \_ DDE \_**](wm-dde-poke.md)訊息。 伺服器應該忽略成員。

如果伺服器傳送負認可以回應 [**WM \_ dde \_**](wm-dde-poke.md)傳送訊息，則用戶端會負責釋出記憶體 (，但不是由與負值通知相關聯之 **WM \_ \_ DDE** 訊息所參考的 *lParam* 參數) 。

## <a name="establishing-a-permanent-data-link"></a>建立永久資料連結

用戶端應用程式可以使用 DDE，在伺服器應用程式中建立專案的連結。 建立這類連結之後，伺服器會將連結專案的定期更新傳送至用戶端，通常是每當專案的值變更時。 因此，會在兩個應用程式之間建立永久資料流程;此資料流程會維持在原處，直到明確地中斷連接為止。

### <a name="initiating-a-data-link"></a>起始資料連結

用戶端會藉由張貼 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息來起始資料連結，如下列範例所示。


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



在此範例中，用戶端應用程式會將 [**WM \_ DDE \_ 建議**](wm-dde-advise.md)訊息的 **FDeferUpd** 旗標設定為 **FALSE**。 這會指示伺服器應用程式在資料變更時，將資料傳送給用戶端。

如果伺服器無法服務 [**WM \_ dde \_ 建議**](wm-dde-advise.md) 要求，它會傳送負的 [**wm \_ dde \_**](wm-dde-ack.md) 通知訊息給用戶端。 但是，如果伺服器具有專案的存取權，而且可以使用要求的格式來轉譯，則伺服器會注意到新的連結 (重新叫用 *hOptions*) 參數中指定的旗標，並傳送給用戶端一個正的 **WM \_ DDE \_** 通知訊息。 然後，在用戶端發出相符的 [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) 訊息之前，伺服器會在每次伺服器中專案的值變更時，將新的資料傳送給用戶端。

[**WM \_ DDE \_ 建議**](wm-dde-advise.md)訊息會建立連結期間要交換的資料格式。 如果用戶端嘗試使用相同的專案建立另一個連結，但使用不同的資料格式，伺服器可以選擇拒絕第二個資料格式，或嘗試支援它。 如果已為任何資料項目建立暖連結，伺服器一次只能支援一種資料格式。 這是因為暖連結的 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息有 **Null** 資料控制碼，否則會包含格式資訊。 因此，伺服器必須拒絕已連結專案的所有暖連結，並且必須拒絕具有暖連結之專案的所有連結。 另一項轉譯可能是當要求相同資料項目的第二個連結時，伺服器會變更連結的格式和經常性存取狀態。

一般而言，用戶端應用程式不應該嘗試一次為數據項建立多個連結。

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>使用貼上連結命令起始資料連結

支援經常性存取或暖資料連結的應用程式通常支援名稱為 Link 的已註冊剪貼簿格式。 當與應用程式的複製和貼上連結命令相關聯時，此剪貼簿格式可讓使用者在應用程式之間建立 DDE 交談，只要複製伺服器應用程式中的資料項目，然後將它貼入用戶端應用程式即可。

當使用者從 [**編輯**] 功能表中選擇 [**複製**] 命令時，伺服器應用程式會將包含應用程式、主題和專案名稱的字串放在剪貼簿中，以支援連結剪貼簿格式。 以下是標準連結格式：

*應用程式 ***\\ 0**_主題_* _\\ 0_*_專案_* 0 _\\ \\ 0_*

單一 null 字元會分隔名稱，而兩個 null 字元會結束整個字串。

用戶端和伺服器應用程式都必須註冊連結剪貼簿格式，如下所示：


```
cfLink = RegisterClipboardFormat("Link");
```



用戶端應用程式透過 [編輯] 功能表上的 [貼上連結] 命令，支援連結剪貼簿格式。 當使用者選擇此命令時，用戶端應用程式會從連結格式的剪貼簿資料剖析應用程式、主題和專案名稱。 使用這些名稱，如果這類交談尚未存在，用戶端應用程式就會起始應用程式和主題的交談。 然後，用戶端應用程式會將 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息傳送至伺服器應用程式，並指定連結格式剪貼簿資料中包含的專案名稱。

以下是當使用者選擇 [貼上] 連結命令時，用戶端應用程式的回應範例。


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



在此範例中，用戶端應用程式會開啟剪貼簿，並判斷它是否包含連結格式的資料 (也就是先前註冊的 cfLink) 。 如果沒有，或如果它無法鎖定剪貼簿中的資料，用戶端會傳回。

在用戶端應用程式抓取剪貼簿資料的指標之後，它會剖析資料以解壓縮應用程式、主題和專案名稱。

用戶端應用程式會判斷主題的交談是否已存在於此主題與伺服器應用程式之間。 如果有交談存在，用戶端會檢查該資料項目是否已有連結。 如果有這類連結，用戶端會向使用者顯示訊息方塊。否則，它會呼叫它自己的 *SendAdvise* 函式，將 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息傳送至該專案的伺服器。

如果用戶端與伺服器之間尚未有主題的交談，用戶端會先呼叫它自己的 *SendInitiate* 函式來廣播 [**WM \_ DDE \_ 初始**](wm-dde-initiate.md) 訊息來要求交談，而第二個呼叫它自己的 *FindServerGivenAppTopic* 函式，以建立與代表伺服器應用程式回應之視窗的交談。 交談開始之後，用戶端應用程式會呼叫 *SendAdvise* 以要求連結。

### <a name="notifying-the-client-that-data-has-changed"></a>通知用戶端資料已變更

當用戶端使用 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息來建立連結時，若 **fDeferUpd** 成員未設定 (也就是在 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) 結構中等於零) ，則用戶端會在每次專案的值變更時，要求伺服器傳送資料項目目。 在這種情況下，伺服器會以先前指定的格式轉譯資料項目的新值，並傳送 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息給用戶端，如下列範例所示。


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



在此範例中，用戶端會適當地處理專案值。 如果已設定專案的 **fAckReq** 旗標，用戶端會傳送正的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給伺服器。

當用戶端建立連結時，若 **fDeferUpd** 成員集 (也就是等於 1) ，用戶端要求每次資料變更時，都只會傳送通知，而不是資料本身。 在這種情況下，當專案值變更時，伺服器不會轉譯該值，而只會傳送具有 null 資料控制碼的 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息給用戶端，如下列範例所示。


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



必要時，用戶端可以藉由發出一般的 [**WM \_ DDE \_ 要求**](wm-dde-request.md) 訊息來要求資料項目的最新值，也可以直接忽略來自伺服器的資料已變更的通知。 在任何一種情況下，如果 **fAckReq** 等於1，用戶端應該會將正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息傳送至伺服器。

### <a name="terminating-a-data-link"></a>終止資料連結

如果用戶端要求終止特定的資料連結，用戶端會傳送 [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) 訊息給伺服器，如下列範例所示。


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



伺服器會檢查用戶端目前是否有此交談中特定專案的連結。 如果連結存在，伺服器就會傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給用戶端，然後再也不需要伺服器傳送專案的相關更新。 如果沒有連結存在，伺服器會傳送負的 **WM \_ DDE \_** 通知訊息給用戶端。

[**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)訊息會指定資料格式。 如果已建立數個熱連結，且每個都使用不同的格式，則零的格式會通知伺服器停止指定專案的所有連結。

若要終止對話的所有連結，用戶端應用程式會使用 null 專案 atom 來傳送具有一個 [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) 訊息的伺服器。 伺服器會判斷交談是否至少有一個目前已建立的連結。 如果連結存在，伺服器就會傳送正面的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息給用戶端，然後伺服器就不再需要傳送對話中的任何更新。 如果沒有連結存在，伺服器會傳送負的 **WM \_ DDE \_** 通知訊息給用戶端。

## <a name="carrying-out-commands-in-a-server-application"></a>在伺服器應用程式中執行命令

應用程式可以使用 [**WM \_ DDE \_ 執行**](wm-dde-execute.md) 訊息，以在另一個應用程式中執行特定命令或一系列的命令。 若要這樣做，用戶端會將包含控制碼的 **WM \_ DDE \_ 執行** 訊息傳送給伺服器，如下列範例所示。


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



在此範例中，伺服器會嘗試執行指定的命令字串。 如果成功，伺服器會傳送正面的 [**wm \_ dde \_**](wm-dde-ack.md) 通知訊息給用戶端; 否則，它會傳送負的 **wm \_ dde 的 \_ ack** 訊息。 這個 **WM \_ dde \_** 通知訊息會重複使用原始 [**WM \_ Dde \_ 執行**](wm-dde-execute.md)訊息中傳遞的 *hCommand* 控制碼。

如果用戶端的命令執行字串要求伺服器終止，伺服器應該藉由傳送正的 [**wm \_ dde \_ 確認**](wm-dde-ack.md) 訊息，然後在結束之前張貼 [**WM \_ dde \_ 終止**](wm-dde-terminate.md) 訊息來回應。 所有以 [**WM \_ dde \_ 執行**](wm-dde-execute.md) 訊息傳送的其他命令都應以同步方式執行; 也就是說，只有在成功完成命令之後，伺服器才應該傳送 **WM \_ dde \_** 通知訊息。

## <a name="terminating-a-conversation"></a>終止交談

用戶端或伺服器可以發出 [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) 訊息，以隨時終止交談。 同樣地，用戶端和伺服器應用程式都應該隨時準備好接收此訊息。 應用程式必須先終止所有的交談，才能關閉。

在下列範例中，終止交談的應用程式會張貼一個 [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) 訊息。


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



這會通知另一個應用程式，傳送應用程式不會傳送任何其他訊息，而且收件者可以關閉其視窗。 在所有情況下，收件者預期會傳送 [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) 訊息來立即回應。 收件者不能傳送負、忙碌或正面的 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息。

在應用程式將 [**WM \_ dde \_ 終止**](wm-dde-terminate.md) 訊息傳送給 DDE 交談中的夥伴之後，它就不能回應來自該夥伴的訊息，因為夥伴可能已損毀傳送回應的目標視窗。

如果應用程式在發佈了 **wm dde \_ dde \_ terminate** 之後，收到非 [**wm \_ dde \_**](wm-dde-terminate.md)的 dde 訊息，則應該釋出與接收訊息相關聯的所有物件，但 **不** 含 **fRelease** 成員的 wm dde [**\_ \_ 資料**](wm-dde-data.md)或 [**WM \_ dde \_**](wm-dde-poke.md)郵件的資料控制碼除外。

當應用程式即將終止時，它應該會在完成 [**WM \_**](/windows/desktop/winmsg/wm-destroy) 終結訊息的處理之前結束所有作用中的 DDE 交談。 但是，如果應用程式未結束其使用中的 DDE 交談，則當視窗損毀時，系統會終止與視窗相關聯的任何 DDE 交談。 下列範例顯示伺服器應用程式如何終止所有 DDE 交談。


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 