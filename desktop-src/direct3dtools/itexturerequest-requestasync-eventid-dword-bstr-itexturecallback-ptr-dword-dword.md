---
description: 要求將材質的內容取得為。DDS (DirectDraw 介面) 檔。
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITextureRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5abfee1b26fd2145aef8e01239cc0b874ee54e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467903"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest：： RequestAsync 方法

要求將材質的內容取得為。DDS (DirectDraw 介面) 檔。

## <a name="syntax"></a>語法


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*eventID*   
指定要比對緩衝區內容的事件 (例如，轉譯目標可能會隨著時間而變更) 。

*textureFileptr*   
材質物件的位址。

*ddsFilename*   
COM 字串，其中包含寫入結果之 dd 檔案的路徑名稱。

*pRequestCallback*   
用來通知主機結果的回呼位址。

*requestCookie*   
可唯一識別要求的 cookie，而且可用來指示它被取消。

*progressIntervalMsecs*   
未使用。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**ITextureRequest**](/windows/desktop/direct3dtools/itexturerequest)

 

 
