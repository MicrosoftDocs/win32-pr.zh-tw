---
description: 要求以指定的來源、資訊清單、參數和指定的框架執行離線分析。
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisRequest：： RequestOfflineAnalysisAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85243b1c07db1f2c30a4e29b221582fd507360f1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624334"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest：： RequestOfflineAnalysisAsync 方法

要求以指定的來源、資訊清單、參數和指定的框架執行離線分析。

## <a name="syntax"></a>語法


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a>參數

*analysisSource*   
指定，其中分析來源來自快取的報表或播放。

*manifestXml*   
COM 字串，其中包含 XML 資訊清單檔的路徑名稱。

*parametersXml*   
COM 字串，其中包含 XML 參數檔案的路徑名稱。

*餅乾*   
可唯一識別要求的 cookie，而且可用來指示它被取消。

*captureFullFileName*   
COM 字串，其中包含 capture 檔案的絕對路徑名稱 ( vsglog) 。

*frameNumber*   
指定的框架。

*outputFullFileName*   
COM 字串，其中包含寫入輸出之檔案的絕對路徑名稱。

*requestCallback*   
用來通知主機結果的回呼位址。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
