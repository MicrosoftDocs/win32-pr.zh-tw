---
description: 檢查產生器是否應該與特定屬性相關聯。
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: IProvidePropertyBuilder：： MapPropertyToBuilder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995619"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>IProvidePropertyBuilder：： MapPropertyToBuilder 方法

檢查產生器是否應該與特定屬性相關聯。

## <a name="syntax"></a>語法


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dispid* \[在\]
</dt> <dd>

有問題的屬性 DISPID。

</dd> <dt>

*pdwCtlBldType* \[擴展\]
</dt> <dd>

要對應的 builder。 這個參數可以是下列值的組合。



| 值                                                                                                                                                                                                                                                          | 意義                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | 在 Visual Studio) 中不支援叫用標準系統產生器 (。<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | 叫用自訂產生器。<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | Builder 會修改物件。 這是常見的行為。<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[擴展\]
</dt> <dd>

識別此屬性之產生器的 GUID。

</dd> <dt>

*builderAvailable* \[退出，retval\]
</dt> <dd>

如果這個屬性目前支援產生器，此參數為 **TRUE** 。

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

 

 




