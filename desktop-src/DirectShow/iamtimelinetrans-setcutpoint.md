---
description: SetCutPoint 方法會設定當轉換轉譯為剪下時，轉換從某個來源剪下的時間。
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'IAMTimelineTrans：： SetCutPoint 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998395"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>IAMTimelineTrans：： SetCutPoint 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetCutPoint`如果轉換是轉譯為剪下，則方法會設定轉換從某個來源減少到下一個來源的時間。

## <a name="syntax"></a>語法


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TLTime* 
</dt> <dd>

相對於開始轉換起點的剪下（以 100-毫微秒單位）。 如果值落在轉換範圍之外，則會截斷為最接近的有效時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

根據預設，剪點是轉換的中間。 例如，在橫跨1秒的轉換中，預設的剪下點在轉換中是0.5 秒。

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

[**IAMTimelineTrans 介面**](iamtimelinetrans.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




