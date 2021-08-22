---
description: 只有當系統正在64位的電腦上執行時，安裝程式才會將 VersionNT64 屬性設定為作業系統的版本號碼。
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285f97a6325df65ace9ff6620489697e6eeeb573761437bd0a826dec4dc31e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526928"
---
# <a name="versionnt64-property"></a>VersionNT64 屬性

只有當系統正在64位的電腦上執行時，安裝程式才會將 **VersionNT64** 屬性設定為作業系統的版本號碼。 如果作業系統不是64位，則屬性是未定義的。

此值為整數： MajorVersion \* 100 + MinorVersion。

基於相容性的理由，如果 [**範本摘要**](template-summary.md)內容指出封裝適用于32位 intel (x86) 系統，且作業系統無法執行64位 intel (x64) 程式碼（例如 ARM Windows 10 ARM64 (上的) ），則屬性也是未定義的。

> [!NOTE]
> 從 Windows 10 組建21277，Windows Insider Preview 計畫的開發人員通道中的 ARM64 組建支援 x64 應用程式。 在這些 ARM64 組建中，會針對 x86 套件定義 VersionNT64 屬性。

## <a name="remarks"></a>備註

條件運算式會測試64位 Windows 簡單的方法是使用屬性名稱，或使用比較運算子來驗證版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式，請參閱[Windows Installer Run-Time](windows-installer-portal.md) Windows 版本所需的最小 Windows Installer service pack 資訊的需求。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




