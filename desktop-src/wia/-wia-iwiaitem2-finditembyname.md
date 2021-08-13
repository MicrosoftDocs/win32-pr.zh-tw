---
description: 使用名稱做為搜尋索引鍵，在專案的子專案樹狀目錄中搜尋。
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'IWiaItem2：： FindItemByName 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5ef0ffdf710d36d2d6c515352bf441e9c66ae169400528db5d5943e2114fefd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440406"
---
# <a name="iwiaitem2finditembyname-method"></a>IWiaItem2：： FindItemByName 方法

使用名稱做為搜尋索引鍵，在專案的子專案樹狀目錄中搜尋。

## <a name="syntax"></a>語法


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*bstrFullItemName* \[在\]
</dt> <dd>

類型： **BSTR**

指定要搜尋之專案的名稱。

</dd> <dt>

*ppIWiaItem2* \[擴展\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

接收找到之專案的 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法會使用名稱做為搜尋索引鍵，來搜尋目前專案的子專案樹狀結構。 如果 **IWiaItem2：： FindItemByName** 找到 *bstrFullItemName* 所指定的專案，它會將指標的位址儲存至 *PpIWiaItem2* 參數中專案的 [**IWiaItem2**](-wia-iwiaitem2.md)介面。

應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
