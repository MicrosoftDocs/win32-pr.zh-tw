---
description: 建立新的子專案。 將 IWiaItem2 物件新增至裝置的 IWiaItem2 樹狀目錄。
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'IWiaItem2：： CreateChildItem 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e7d7215f528c36f6b4f5883be19d5d37c8b76d4d8ad9cacbcaa7a63397337c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965567"
---
# <a name="iwiaitem2createchilditem-method"></a>IWiaItem2：： CreateChildItem 方法

建立新的子專案。 將 [**IWiaItem2**](-wia-iwiaitem2.md) 物件新增至裝置的 **IWiaItem2** 樹狀目錄。

## <a name="syntax"></a>語法


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lItemFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定 WIA 2.0 專案類型。 請參閱 [**WIA 專案類型旗標**](-wia-wia-item-type-flags.md)。

</dd> <dt>

*lCreationFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定如何建立新專案。

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0) 


</dt> <dd>

設定子系屬性的預設值。

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**複製 \_父 \_ 屬性 \_ 值** (0x40000000) 


</dt> <dd>

從父系複製所有讀取/寫入屬性的值。

</dd> </dl> </dd> <dt>

*bstrItemName* \[在\]
</dt> <dd>

類型： **BSTR**

指定專案名稱。 這個名稱會附加至父專案名稱的結尾，以產生完整的專案名稱。

</dd> <dt>

*ppIWiaItem2* \[擴展\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

接收 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標位址，此介面會設定 **IWiaItem2：： CreateChildItem** 方法。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

某些 WIA 2.0 硬體裝置可讓應用程式在代表裝置的 [**IWiaItem2**](-wia-iwiaitem2.md) 樹狀結構中建立新專案。 應用程式必須測試裝置，才能查看是否支援這項功能。 使用 IEnumWIA \_ DEV \_ CAPS 介面來列舉目前裝置的功能。

如果裝置允許在 [**IWiaItem2**](-wia-iwiaitem2.md) 樹狀結構中建立新專案，則叫用 **IWiaItem2：： CreateChildItem** 會建立新的 **IWiaItem2** 物件，該物件為目前節點的子系。 它會透過 *ppIWiaItem2* 參數，將新節點的指標傳遞至應用程式。 應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

如果 *lCreationFlags* 是複製 \_ 父 \_ 屬性 \_ 值， *而 lItemFlags* 為零，則函數會傳回 E \_ INVALIDARG。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
