---
description: SplitAt2 方法會在指定的時間分割物件。 這個方法相當於 IAMTimelineSplittable：： SplitAt，但會接受 REFTIME 值。
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'IAMTimelineSplittable：： SplitAt2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9c3a5720ade42291037611c155c2cb9e834f0734e7af6e2c36277c409592143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904908"
---
# <a name="iamtimelinesplittablesplitat2-method"></a>IAMTimelineSplittable：： SplitAt2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SplitAt2`方法會在指定的時間分割物件。 這個方法相當於 [**IAMTimelineSplittable：： SplitAt**](iamtimelinesplittable-splitat.md)，但會接受 [**REFTIME**](reftime.md) 值。

## <a name="syntax"></a>語法


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Time* 
</dt> <dd>

分割物件的時間，相對於時間軸的開始時間（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下：



| 傳回碼                                                                                   | 描述                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | 沒有要分割的專案。<br/>                       |
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 此物件目前不存在。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineSplittable 介面**](iamtimelinesplittable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




