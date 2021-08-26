---
description: 非同步要求，以取得在圖形記錄檔中所捕捉的清單方塊架。
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameListRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b1161f36a2bb0d1cdc9e1f65fa2ce3fea4984f00
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621974"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>IFrameListRequest：： RequestAsync 方法

非同步要求，以取得在圖形記錄檔中所捕捉的清單方塊架。

## <a name="syntax"></a>語法


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*requestCallback*   
用來通知主機結果的回呼位址。

*requestCookie*   
可唯一識別要求的 cookie，而且可用來指示它被取消。

*progressIntervalMsecs*   
未使用。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IFrameListRequest**](/windows/desktop/direct3dtools/iframelistrequest)

 

 
