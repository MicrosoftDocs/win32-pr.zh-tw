---
description: 指定代表感應器轉換所需裝置功能的 unicode 字串清單。
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: 'MF_DEVICESTREAM_REQUIRED_CAPABILITIES 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113673"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>MF \_ DEVICESTREAM \_ 需要的 \_ 功能屬性

指定代表感應器轉換所需裝置功能的 unicode 字串清單。

## <a name="data-type"></a>資料類型

**WCHAR \** _

## <a name="remarks"></a>備註

這個屬性是選擇性的，只有在感應器轉換存取受保護的資源時才需要。 此值必須是 [_ *DeviceCapability* *](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability)中定義的字串標記清單（以分號分隔）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



 

 
