---
description: GetDefaultFPS 方法會捕獲來源物件的預設畫面播放速率。 如果轉譯引擎無法判斷原始來源的畫面播放速率，則會使用此值。
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'IAMTimelineSrc：： GetDefaultFPS 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989248"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>IAMTimelineSrc：： GetDefaultFPS 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetDefaultFPS`方法會捕獲來源物件的預設畫面播放速率。 如果轉譯引擎無法判斷原始來源的畫面播放速率，則會使用此值。

## <a name="syntax"></a>語法


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFPS* 
</dt> <dd>

接收預設畫面播放速率（以每秒畫面格數為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果檔案格式指定畫面播放速率，則不需要預設的畫面播放速率。 這是音訊和影片格式的情況。

如果來源是點陣圖或 JPEG 影像，轉譯引擎會使用它做為與裝置無關的點陣圖中的第一個影像， (DIB) 序列，且畫面播放速率等於預設的畫面播放速率。 若要呈現靜態影像，而不是 DIB 順序，請將預設畫面播放速率設定為0。

如果來源為 GIF，請勿設定畫面播放速率。 若為動畫 Gif，GIF 檔案會指定每個影像之間的延遲。

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

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




