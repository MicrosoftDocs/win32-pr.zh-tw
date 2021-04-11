---
description: CIM PCMCIAController 類別的 Reset 方法會 \_ 要求重設邏輯裝置。
ms.assetid: c58e3265-2849-4154-a03e-2e1cfa9e3d30
ms.tgt_platform: multiple
title: CIM_PCMCIAController 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8576bc5c1ce291c355d2907761e5b342ea6f3bc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187739"
---
# <a name="reset-method-of-the-cim_pcmciacontroller-class"></a>CIM PCMCIAController 類別的 Reset 方法 \_

CIM PCMCIAController 類別的 **reset** 方法會 \_ 要求重設邏輯裝置。 這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

## <a name="syntax"></a>語法


```mof
uint32 Reset();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果要求已成功執行，則傳回 0 (零) ，如果要求不受支援則為 1 (一個) ，如果發生錯誤，則會傳回另一個值。

## <a name="remarks"></a>備註

這個方法不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。 針對衍生自 [**CIM \_ PCMCIACONTROLLER**](cim-pcmciacontroller.md)的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。

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

[CIM \_ PCMCIAController](reset-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> </dl>

 

 




