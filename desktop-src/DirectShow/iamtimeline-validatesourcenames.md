---
description: ValidateSourceNames 方法會使用媒體定位器來驗證時間軸中的來源名稱。 （選擇性）此方法也會更新找到檔案的任何來源物件。
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'IAMTimeline：： ValidateSourceNames 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976155"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>IAMTimeline：： ValidateSourceNames 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ValidateSourceNames`方法會使用媒體定位器來驗證時間軸中的來源名稱。 （選擇性）此方法也會更新找到檔案的任何來源物件。

## <a name="syntax"></a>語法


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ValidateFlags* 
</dt> <dd>

指定媒體定位器行為的 [**檔案名驗證旗標**](file-name-validation-flags.md) 的位元組合。 SFN \_ VALIDATEF \_ REPLACE 和 SFN \_ VALIDATEF \_ CHECK flags 必須存在，否則方法會傳回 E \_ INVALIDARG。

</dd> <dt>

*pOverride* 
</dt> <dd>

要用來取代預設值之媒體定位器 [**IMediaLocator**](imedialocator.md) 介面的選擇性指標。 若要使用預設媒體定位器，請將此參數的值設定為 **Null**。 如需詳細資訊，請參閱「備註」。

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

事件的控制代碼。 方法會在事件完成驗證之後發出信號。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用 *pOverride* 參數，您可以提供自己自訂的 [**IMediaLocator**](imedialocator.md) 介面實作為。 例如，預設媒體定位器將不會通知您的應用程式 (找到的檔案，或找不到) 。 若要解決這項限制，您可以執行自訂媒體定位器，使其成為預設版本的包裝函式。 在您的自訂版本中，將 [**IMediaLocator：： FindMediaFile**](imedialocator-findmediafile.md) 呼叫直接傳遞至預設版本，並檢查傳回值。

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

[**IAMTimeline 介面**](iamtimeline.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




