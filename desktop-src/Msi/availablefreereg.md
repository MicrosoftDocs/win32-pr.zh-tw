---
description: AVAILABLEFREEREG 屬性會在呼叫 AllocateRegistrySpace 動作之後，以 kb 為單位指定登錄中的可用空間總計（以 kb 為單位）。AVAILABLEFREEREG 屬性的最大值為 2000000 kb。這個屬性只會設定在 Windows 2000。
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: AVAILABLEFREEREG 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45508494f9ba87ec8261b38ea18f83d0b3ad9796f7390b70349211cbf244df3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650068"
---
# <a name="availablefreereg-property"></a>AVAILABLEFREEREG 屬性

**AVAILABLEFREEREG** 屬性會在呼叫 [AllocateRegistrySpace 動作](allocateregistryspace-action.md)之後，以 kb 為單位指定登錄中的可用空間總計（以 kb 為單位）。

**AVAILABLEFREEREG** 屬性的最大值為 2000000 kb。

這個屬性只會設定在 Windows 2000。

## <a name="remarks"></a>備註

**AVAILABLEFREEREG** 屬性必須設定為夠大的值，以確保登錄中的足夠空間可供安裝所加入的所有註冊資訊使用。 確保足夠空間所需的最小值取決於 [AllocateRegistrySpace 動作](allocateregistryspace-action.md) 在動作順序中的 [位置，因為](registry-table.md)安裝程式會在登錄、 [類別](class-table.md)、 [SelfReg](selfreg-table.md)、 [延伸](extension-table.md)模組、 [MIME](mime-table.md)和 [動詞](verb-table.md) 資料表中註冊資訊時，自動增加所需的空間。 安裝程式不會將登錄空間總數增加至 **AVAILABLEFREEREG** 所指定的數量，直到達到動作順序中的 AllocateRegistrySpace 為止。

如果 AllocateRegistrySpace 是動作順序中的第一個動作，則應該將 **AVAILABLEFREEREG** 設定為登錄資料表、類別資料表、TypeLib 資料表、SelfReg 資料表、延伸模組資料表、MIME 資料表、動詞資料表、 [自訂動作](custom-actions.md) 註冊、自我註冊，以及安裝期間所寫入的任何其他登錄資訊所需的總空間。 **AVAILABLEFREEREG** 的值是安裝所加入的總資訊量，可確保所有情況下都有足夠的空間。 這也是最常見的情況。

如果 AllocateRegistrySpace 動作可以在寫入註冊資料的所有 [標準動作](standard-actions.md) （例如 [WriteRegistryValues](writeregistryvalues-action.md) 和 [RegisterClassInfo](registerclassinfo-action.md)）之後，于動作順序中撰寫，則 **AVAILABLEFREEREG** 需求的值只會設定為註冊自訂動作、註冊類型程式庫，以及尚未透過資料表註冊之任何其他資訊的必要空間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




