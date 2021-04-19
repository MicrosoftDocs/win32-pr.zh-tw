---
description: SetSourceNameValidation 方法會指定轉譯引擎如何驗證檔案名。
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'IRenderEngine：： SetSourceNameValidation 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990935"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a>IRenderEngine：： SetSourceNameValidation 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetSourceNameValidation`方法會指定轉譯引擎如何驗證檔案名。

## <a name="syntax"></a>語法


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FilterString* 
</dt> <dd>

包含篩選字串配對的 **BSTR** 值，格式為 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrFilter** 成員所需。 如果媒體定位器向終端使用者顯示 [開啟檔案] 對話方塊，則會使用此篩選器。

</dd> <dt>

*pOverride* 
</dt> <dd>

要用來取代預設值之媒體定位器 [**IMediaLocator**](imedialocator.md) 介面的選擇性指標。 若要使用預設媒體定位器，請將此參數的值設定為 **Null**。 如需詳細資訊，請參閱「備註」。

</dd> <dt>

*旗標* 
</dt> <dd>

指定媒體定位器行為的 [**檔案名驗證旗標**](file-name-validation-flags.md) 的位元組合。 \_ \_ 必須要有 SFN VALIDATEF 檢查旗標。 \_ \_ 使用這個方法時，SFN VALIDATEF hlinkMUTED 旗標沒有任何作用。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                            | Description                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>                            |
| <dl> <dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt> </dl> | 轉譯引擎無法初始化。<br/> |



 

## <a name="remarks"></a>備註

使用 *pOverride* 參數，您可以提供自己自訂的 [**IMediaLocator**](imedialocator.md) 介面實作為。 例如，預設媒體定位程式不會通知應用程式找到 (的檔案，或找不到) 。 若要解決這項限制，您可以執行自訂媒體定位器，使其成為預設版本的包裝函式。 然後，將 [**IMediaLocator：： FindMediaFile**](imedialocator-findmediafile.md) 呼叫直接傳遞至預設版本，並檢查傳回值。

目前，這個方法不會驗證動態載入的來源。 請參閱 [**IRenderEngine：： SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)。

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

[**IRenderEngine 介面**](irenderengine.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 
