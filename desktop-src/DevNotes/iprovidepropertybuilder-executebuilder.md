---
description: 通知物件應針對指定的屬性顯示其產生器。
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: IProvidePropertyBuilder：： ExecuteBuilder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975974"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>IProvidePropertyBuilder：： ExecuteBuilder 方法

通知物件應針對指定的屬性顯示其產生器。

## <a name="syntax"></a>語法


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dispid* \[在\]
</dt> <dd>

產生器所顯示的屬性 DISPID。

</dd> <dt>

*bstrGuidBldr* \[在\]
</dt> <dd>

要叫用之產生器 GUID 的 **BSTR** 。 這會從 [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md)傳回。

</dd> <dt>

*pdispApp* \[在\]
</dt> <dd>

設定為 **Null**。

</dd> <dt>

*hwndBldrOwner* \[在\]
</dt> <dd>

父代彈出產生器視窗的控制碼。

</dd> <dt>

*pvarValue* \[in、out\]
</dt> <dd>

屬性的目前值。 如果 *pbActionCommitted* 為 TRUE，則物件可以修改此值，並將新值變更為 **TRUE**。

</dd> <dt>

*pbActionCommitted* \[退出，retval\]
</dt> <dd>

值，這個值會指出 builder 是否在物件上執行動作。 可以在使用者修改某個內容時使用，然後在快顯產生器對話方塊上按 [確定]。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




