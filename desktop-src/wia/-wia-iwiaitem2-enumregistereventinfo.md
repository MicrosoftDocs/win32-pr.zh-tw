---
description: IWiaItem2：： EnumRegisterEventInfo 方法會建立一個列舉值，您可以使用它來取得已註冊應用程式之事件的相關資訊。
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2：： EnumRegisterEventInfo 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a81f342713bcb3e58521856aa84561c000dcc5e0d05112bc9586514a5469bfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035020"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>IWiaItem2：： EnumRegisterEventInfo 方法

**IWiaItem2：： EnumRegisterEventInfo** 方法會建立一個列舉值，您可以使用它來取得已註冊應用程式之事件的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

未使用。 設定為0。

</dd> <dt>

*pEventGUID* \[在\]
</dt> <dd>

類型： **CONST GUID \***

識別碼的指標，指定您要取得註冊資訊的硬體事件。

</dd> <dt>

*ppIEnum* \[擴展\]
</dt> <dd>

類型： **[ **IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

[**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)介面指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

應用程式會呼叫這個方法來建立事件資訊的列舉值物件。 **IWiaItem2：： EnumRegisterEventInfo** 會在 *ppIEnum* 參數中儲存列舉值物件的 [**IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)介面位址。 然後，程式會使用介面指標來列舉所註冊之事件的屬性。

應用程式必須在透過 *ppIEnum* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl> |



 

 
