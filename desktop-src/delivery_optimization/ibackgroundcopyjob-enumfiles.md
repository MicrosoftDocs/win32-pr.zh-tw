---
title: 'IBackgroundCopyJob EnumFiles 方法 (>deliveryoptimization .h) '
description: 抓取 IEnumBackgroundCopyFiles 介面指標，您可用來列舉作業中的檔案。
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- EnumFiles 方法
- EnumFiles 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，EnumFiles 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ecd27e1de8dfaa16d7f5d2dc3218d3c993148a0878976e329b4953cefdc4c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543014"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>IBackgroundCopyJob：： EnumFiles 方法

抓取 [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) 介面指標，您可用來列舉作業中的檔案。

## <a name="syntax"></a>語法


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnumFiles* \[擴展\]
</dt> <dd>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) 介面指標，用來列舉作業中的檔案。 完成時釋放 *ppEnumFiles* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





