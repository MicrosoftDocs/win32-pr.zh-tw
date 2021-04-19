---
description: 只有當系統正在64位的電腦上執行時，安裝程式才會將 VersionNT64 屬性設定為作業系統的版本號碼。
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998771"
---
# <a name="versionnt64-property"></a>VersionNT64 屬性

只有當系統正在64位的電腦上執行時，安裝程式才會將 **VersionNT64** 屬性設定為作業系統的版本號碼。 如果作業系統不是64位，則屬性是未定義的。

此值為整數： MajorVersion \* 100 + MinorVersion。

基於相容性的理由，如果 [**範本摘要**](template-summary.md) 內容指出封裝適用于32位 Intel 系統，且作業系統是不是 Intel64 或 x64 (的64位架構（例如 ARM64) ），則屬性也是未定義的。

## <a name="remarks"></a>備註

條件運算式會測試64位 Windows，只要使用屬性名稱，或是使用比較運算子來驗證版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Installer 在 Windows Server 2003 或 Windows XP 上，請參閱 Windows Installer Run-Time Windows Installer 版本所需的最低 Windows service pack 相關資訊的 [需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




