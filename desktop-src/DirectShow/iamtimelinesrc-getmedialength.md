---
description: GetMediaLength 方法會抓取此來源物件的媒體長度。
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'IAMTimelineSrc：： GetMediaLength 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977561"
---
# <a name="iamtimelinesrcgetmedialength-method"></a>IAMTimelineSrc：： GetMediaLength 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetMediaLength` 此來源物件的媒體長度。

## <a name="syntax"></a>語法


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLength* 
</dt> <dd>

以 100-毫微秒單位接收媒體長度。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                     | Description                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>            | 成功。<br/>                                |
| <dl> <dt>**E \_ NOTDETERMINED**</dt> </dl> | 未在這個物件上設定媒體時間。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>       | **Null** 指標引數。<br/>              |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineSrc 介面**](iamtimelinesrc.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




