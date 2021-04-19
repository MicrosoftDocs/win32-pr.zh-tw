---
title: '篩選權數識別碼 (Fwpmu .h) '
description: 基礎篩選引擎 (BFE) 用來計算自動產生之篩選加權的篩選權數識別碼。
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967992"
---
# <a name="filter-weight-identifiers"></a>篩選權數識別碼

基礎篩選引擎 (BFE) 用來計算自動產生之篩選權數的篩選權數識別碼，如下所示。

如需篩選權數產生的詳細資訊，請參閱 [篩選權數指派](filter-weight-assignment.md) 。

<dl> <dt>

<span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM \_ 自動 \_ 權數 \_ 位**
</dt> <dd> <dl> <dt>

 (60) 
</dt> <dt>



用於自動產生之篩選加權的位數。


</dt> </dl> </dd> <dt>

<span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM \_ 自動 \_ 加權 \_ 最大值**
</dt> <dd> <dl> <dt>

 (**MAXUINT64** >> 4) 
</dt> <dt>



自動產生的篩選權數上限。


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**
</dt> <dd> <dl> <dt>

 (0xC) 
</dt> <dt>



BFE 會將具有此範圍值的權數指派給 IKE 和 AuthIP 篩選器。

如需 IKE/AuthIP 篩選器的詳細資訊，請參閱 [ike/Authip 豁免](ike-exemptions.md) 。


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM \_ 權數 \_ 範圍 \_ IPSEC**
</dt> <dd> <dl> <dt>

(0x0)
</dt> <dt>



BFE 會將具有此範圍值的權數指派給 IPsec 原則篩選器。


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM \_ 權數 \_ 範圍 \_ 最大值**
</dt> <dd> <dl> <dt>

 (**MAXUINT64** >> 60) 
</dt> <dt>



允許的篩選權數範圍值上限。


</dt> </dl> </dd> </dl>

> [!Note]  
> **MAXUINT64** 代表 **UINT64** 的最大可能值。 這個常數的值為0xFFFFFFFFFFFFFFFF。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Fwpmu。h</dt> </dl> |



 

 





