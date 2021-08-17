---
description: 確認參考的實體元素是否可包含或插入實體封裝中。
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: CIM_PhysicalPackage 類別的 IsCompatible 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8479ce400fb9c4e52d51f9834ffbc7c1d57d7a44d21ebf37c88149c826911409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834655"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a>CIM PhysicalPackage 類別的 IsCompatible 方法 \_

**IsCompatible** 方法會驗證參考的實體元素是否可包含或插入實體封裝中。 在子類別中，可以使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。 您也可以在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ElementToCheck* \[在\]
</dt> <dd>

**IsCompatible** 方法執行所在實體元素的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。

## <a name="remarks"></a>備註

這個方法目前不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ PhysicalPackage**](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)
</dt> </dl>

 

