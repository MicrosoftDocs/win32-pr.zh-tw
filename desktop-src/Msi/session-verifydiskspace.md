---
description: VerifyDiskSpace 屬性是唯讀屬性。
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: VerifyDiskSpace 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991351"
---
# <a name="sessionverifydiskspace-property"></a>VerifyDiskSpace 屬性

**VerifyDiskSpace** 屬性是唯讀屬性。 如果有足夠的磁碟空間，則會傳回 true，如果磁片已滿，則會傳回 false。 因為此屬性會使用由成本動作所收集的資訊，所以應該只在 [CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和 [CostFinalize 動作](costfinalize-action.md)之後呼叫 **VerifyDiskSpace** 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




