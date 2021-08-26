---
description: 設定在來源解析期間建立 PMP 媒體會話的回呼。
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: 'MFPKEY_PMP_Creation_Callback 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655d61865eaecd89fa84664fc5c25f89762180ac9007e21cc7cbc98f7a68b056
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953858"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>MFPKEY \_ PMP \_ 建立 \_ 回呼屬性

設定在來源解析期間建立 [PMP 媒體會話](pmp-media-session.md) 的回呼。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**IUnknown\***

VT \_ 不明

**punkVal**



## <a name="remarks"></a>備註

某些受保護的內容可能需要使用此屬性。 如果是，來源解析程式會失敗，並出現錯誤碼 **MF \_ E \_ 解析度 \_ 需要 \_ PMP \_ 建立 \_ 回呼**。

若要使用這個屬性，請執行下列動作。

1.  呼叫 [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) 以建立屬性存放區。
2.  執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 回呼介面。
3.  在 \_ \_ \_ 屬性存放區上設定 MFPKEY PMP 建立回呼屬性。 值是 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 執行的指標。
4.  呼叫 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)。 將指標傳入 *pProps* 參數中的屬性存放區。

在回呼介面的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法中，執行下列動作。

1.  呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) 來建立 [PMP 媒體會話](pmp-media-session.md)。
2.  將 PMP 媒體會話上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 呼叫至 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 介面的指標。
3.  針對在 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)的 *pAsyncResult* 參數中傳遞的結果物件，呼叫 [**IMFAsyncResult：： >getstate**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) 。 查詢傳回的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標以取得 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。
4.  使用下列參數呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ：
    -   *dwQueue*： **MFASYNC \_ 回呼 \_ 佇列 \_ 標準**
    -   *pCallback*：在步驟3中取得的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 指標。
    -   *pState*：在步驟2中取得的 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[PMP 媒體會話](pmp-media-session.md)
</dt> <dt>

[受保護的媒體路徑](protected-media-path.md)
</dt> <dt>

[來源解析程式](source-resolver.md)
</dt> </dl>

 

 
