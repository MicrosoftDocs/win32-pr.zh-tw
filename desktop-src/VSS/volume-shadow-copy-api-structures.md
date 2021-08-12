---
description: 下列結構會在磁片區陰影複製 API 中定義。
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: 磁片區陰影複製 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f95527f505430e0283b44d233605febb5695cada3f9740e850945f58e751f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590550"
---
# <a name="volume-shadow-copy-api-structures"></a>磁片區陰影複製 API 結構

下列結構會在磁片區陰影複製 API 中定義。



| 結構                                                           | 描述                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | 包含指定元件的相關資訊。                                                                                                                                                                                                                       |
| [**VSS \_ 差異 \_ 區域的比較 \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | 描述來源磁片區之間的關聯，包含原始檔案資料和包含陰影複製存放區域的磁片區。                                                                                                                                |
| [**VSS \_ DIFF 磁片區的比較 \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | 描述陰影複製存放區磁片區。                                                                                                                                                                                                                        |
| [**VSS \_ 管理 \_ 物件的 \_ 主張**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | 描述磁片區、陰影複製存放磁片區或陰影複製存放區的屬性。                                                                                                                                                                    |
| [**VSS \_ 管理 \_ 物件聯 \_ 集**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Vss [**\_ 管理 \_ 物件 \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)的結構所使用的 [**vss \_ 磁片 \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)區架構、 [**vss \_ 差異 \_ \_ 磁片**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)[**區和 vss \_ 差異 \_ 區域 \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)架構的聯集。 |
| [**VSS \_ 物件的 \_ 主張**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | 描述提供者、磁片區、陰影複製或陰影複製集的屬性。                                                                                                                                                                                    |
| [**VSS \_ 物件聯 \_ 集**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Vss [**\_ \_ 物件**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)架構結構所使用的 [**Vss \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集架構和 [**vss \_ 提供者 \_**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)架構的聯集。                                                                    |
| [**VSS \_ 提供者的 \_ 主張**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | 指定陰影複製提供者屬性。                                                                                                                                                                                                                          |
| [**VSS \_ 快照 \_ 集**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | 包含陰影複製或陰影複製集的屬性。                                                                                                                                                                                                        |
| [**VSS \_ 磁片區的 \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | 描述陰影複製來源磁片區的屬性。                                                                                                                                                                                                            |
| [**VSS \_ 磁片區 \_ 保護 \_ 資訊**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | 包含磁片區陰影禁止複製層級的相關資訊。                                                                                                                                                                                                 |



 

 

 



