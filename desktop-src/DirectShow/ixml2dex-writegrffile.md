---
description: WriteGrfFile 方法會將篩選圖形寫入 grf 格式的檔案。
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'IXml2Dex：： WriteGrfFile 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995316"
---
# <a name="ixml2dexwritegrffile-method"></a>IXml2Dex：： WriteGrfFile 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `WriteGrfFile` 篩選圖形寫入 grf 格式的檔案。

## <a name="syntax"></a>語法


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGraph* 
</dt> <dd>

篩選圖形的 **IUnknown** 介面指標。

</dd> <dt>

*FileName* 
</dt> <dd>

字串，指定要寫入的檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值，此值相依于介面的執行。 HRESULT 可以包含下列其中一個標準常數，或其他未列出的值。



| 傳回碼                                                                                  | Description                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 失敗。<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 引數無效。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>             |



 

這個方法也會傳回由內部呼叫 **IStorage：： CreateStream** 和 **IPersist：： Save** 方法所產生的錯誤碼。 如需詳細資訊，請參閱 Platform SDK。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Internet Explorer 4.0 或更新版本<br/>                                               |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IXml2Dex 介面**](ixml2dex.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




