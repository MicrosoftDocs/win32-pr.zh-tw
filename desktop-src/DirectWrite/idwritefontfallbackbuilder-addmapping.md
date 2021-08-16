---
title: IDWriteFontFallbackBuilder AddMapping 方法
description: 將單一對應附加至清單。 針對每個額外的對應呼叫一次。
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- AddMapping 方法直接寫入
- AddMapping 方法 Direct Write，IDWriteFontFallbackBuilder 介面
- IDWriteFontFallbackBuilder 介面 Direct Write，AddMapping 方法
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6496ac9ef9bdfa574cc2c4710ed4620fd855dbf5eff2b22885b32bf343d141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650438"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>IDWriteFontFallbackBuilder：： AddMapping 方法

將單一對應附加至清單。 針對每個額外的對應呼叫一次。

## <a name="syntax"></a>語法


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*範圍* 
</dt> <dd>

類型： **[ **DWRITE \_ UNICODE \_ 範圍**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\***

適用于此對應的 Unicode 範圍。

</dd> <dt>

*rangesCount* 
</dt> <dd>

類型： **UINT32**

Unicode 範圍的數目。

</dd> <dt>

*targetFamilyNames* \[在\]
</dt> <dd>

Type： **CONST WCHAR \* \***

目標系列名稱字串的清單。

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

類型： **UINT32**

目標系列名稱的數目。

</dd> <dt>

*fontCollection* \[在中，選擇性\]
</dt> <dd>

類型： **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

這個對應的選擇性明確字型集合。

</dd> <dt>

*>localename* \[在中，選擇性\]
</dt> <dd>

Type： **CONST WCHAR \***

內容的地區設定。

</dd> <dt>

*baseFamilyName* \[在中，選擇性\]
</dt> <dd>

Type： **CONST WCHAR \***

要符合的基底系列名稱（如果適用）。

</dd> <dt>

*scale* 
</dt> <dd>

類型： **FLOAT**

將結果目標字型乘以的縮放因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

