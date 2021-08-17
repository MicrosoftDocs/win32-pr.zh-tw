---
description: 安裝程式物件的 Version 屬性是唯讀屬性，它是目前版本 Windows Installer 的字串表示。 字串會以下列格式傳回。
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: 安裝程式版本屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3d2aeb845647317751eba53caae1609f8d3d66f9f7d373aa7faa24e3b8cdfb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119295543"
---
# <a name="installerversion-property"></a>安裝程式版本屬性

[**安裝程式**](installer-object.md)物件的 **Version** 屬性是唯讀屬性，它是目前版本 Windows Installer 的字串表示。 字串會以下列格式傳回。

*主要*。*次要*。*build*。*更新*

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




