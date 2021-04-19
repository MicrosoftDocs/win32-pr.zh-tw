---
description: 捕獲裝置屬性
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: 捕獲裝置屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991664"
---
# <a name="capture-device-attributes"></a>捕獲裝置屬性

下列是與 capture 裝置相關的屬性：



| 屬性                                                                                                                     | 描述                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [MF \_ DEVSOURCE \_ 屬性 \_ 易記 \_ 名稱](mf-devsource-attribute-friendly-name.md)                                          | 裝置的顯示名稱。                                                          |
| [MF \_ DEVSOURCE \_ 屬性 \_ 媒體 \_ 類型](mf-devsource-attribute-media-type.md)                                                | 裝置的輸出格式。                                                         |
| [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md)                                              | 裝置的類型，例如音訊捕獲或影片捕獲。                         |
| [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 端點 \_ 識別碼](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | 音訊捕獲裝置的端點識別碼。                                        |
| [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 角色](mf-devsource-attribute-source-type-audcap-role.md)                    | 音訊捕獲裝置的裝置角色。                                        |
| [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 類別](mf-devsource-attribute-source-type-vidcap-category.md)            | 影片裝置的裝置類別。                                             |
| [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ HW \_ 來源](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | 指定影片捕獲來源是否為硬體裝置或軟體裝置。 |
| [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 最大 \_ 緩衝區](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | 指定影片捕獲來源將緩衝的最大框架數目。   |
| [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | 影片捕獲驅動程式的符號連結。                                       |
| [\_ \_ \_ 具有 \_ QPC \_ 屬性的 MFT HW TIMESTAMP](mft-hw-timestamp-with-qpc-attribute.md)                                           | 指定裝置來源是否使用時間戳的系統時間。           |



 

這些屬性會搭配下列功能使用：

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 



