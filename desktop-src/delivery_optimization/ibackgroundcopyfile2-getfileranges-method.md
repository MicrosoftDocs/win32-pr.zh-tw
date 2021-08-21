---
title: 'IBackgroundCopyFile2 GetFileRanges 方法 (>deliveryoptimization .h) '
description: 抓取您要從遠端檔案下載的範圍。
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- GetFileRanges 方法
- GetFileRanges 方法，IBackgroundCopyFile2 介面
- IBackgroundCopyFile2 介面，GetFileRanges 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 156bb2eb1e136593bfec4310599200f2d2800e271defa0e4a3259a4a67acb648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047076"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>IBackgroundCopyFile2：： GetFileRanges 方法

抓取您要從遠端檔案下載的範圍。

## <a name="syntax"></a>語法


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RangeCount* \[in、out\]
</dt> <dd>

*範圍* 中的元素數目。

</dd> <dt>

*範圍* \[擴展\]
</dt> <dd>

[**BG_FILE_RANGE**](bg-file-range.md)結構的陣列，指定要下載的範圍。 完成時，請呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函式來釋放 *範圍*。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列傳回值以及其他值。



| 傳回碼                                                                              | 描述                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Success<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | 未指定範圍，或作業為上傳或上傳回復作業。 *RangeCount* 設定為零，而 *範圍* 設定為 **Null**。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 定義為83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

