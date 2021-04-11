---
description: WIA 提供數個介面來列舉各種功能、屬性和資訊。
ms.assetid: d46d4c18-79cc-4f3c-9745-522ab2635068
title: 使用 WIA 枚舉器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee42f99718cb36071b828e87e3a71de6d70ab5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191389"
---
# <a name="using-wia-enumerators"></a>使用 WIA 枚舉器

WIA 提供數個介面來列舉各種功能、屬性和資訊。 Windows 映像取得 (WIA) 列舉介面是標準元件物件模型的特定實作為 (COM) 列舉介面。 如需詳細資訊，請參閱 [IEnumXXXX](/previous-versions//ms680089(v=vs.85))。

下表提供 WIA 列舉介面的相關資訊。 

| 介面                                                   | 如何取得指標                                                                                                                                                                                    | 用於                                                                                                                             |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)       | 呼叫 WIA 根專案的 [**IWiaItem：： EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) 或 [**IWiaItem2：： EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) 方法。 | 列舉 WIA 硬體裝置的功能，例如裝置命令和事件。                                            |
| [**IEnumWIA \_ 開發人員 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)       | 呼叫 [**IWiaDevMgr：： EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) 或 [**IWiaDevMgr2：： EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) 方法。                                            | 列舉可用的 WIA 裝置，並提供其 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面的指標。 |
| [**IEnumWIA \_ 格式 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) | 呼叫專案的 [**IWiaDataTransfer：： idtEnumWIA \_ 格式 \_ 資訊**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info) 方法。                                                                              | 列舉 WIA 專案提供的所有影像格式資訊。                                                                    |
| [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)                   | 呼叫 WIA 專案的 [**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) 或 [**IWiaItem2：： EnumChildItems**](-wia-iwiaitem2-enumchilditems.md) 方法。                                          | 列舉代表裝置或資料夾之 WIA 專案的子專案。                                                |



 

 

 
