---
title: 'IEnumBackgroundCopyFiles Next 方法 (>deliveryoptimization .h) '
description: 擷取列舉型別序列中指定的項目數目。 如果序列中剩餘的元素數目少於所要求的數目，則會抓取剩餘的元素。
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Next 方法
- Next 方法，IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，Next 方法
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dcf24c65b7f282b1a1e15d3109ce1af9ccfc0af6436c80c94760f0b4cd18069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461878"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>IEnumBackgroundCopyFiles：： Next 方法

擷取列舉型別序列中指定的項目數目。 如果序列中剩餘的元素數目少於所要求的數目，則會抓取剩餘的元素。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

要求的元素數目。

</dd> <dt>

*rgelt* \[擴展\]
</dt> <dd>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)物件的陣列。 完成時，您必須釋放 *rgelt* 中的每個物件。

</dd> <dt>

*pceltFetched* \[擴展\]
</dt> <dd>

在 *rgelt* 中傳回的元素數目。 如果 *celt* 是一個，您可以將 *PceltFetched* 設定為 **Null** 。 否則，在呼叫這個方法之前，請先將 *pceltFetched* 的值初始化為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | 描述                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功傳回要求的元素數目。<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | 傳回的數目小於要求的元素數目。<br/>    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





