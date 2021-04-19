---
description: 設定 DISABLEMEDIA 屬性可防止安裝程式將任何媒體來源（例如 CD-ROM）註冊為產品的有效來源。 但是，如果已啟用流覽，使用者仍可流覽至媒體來源。
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: DISABLEMEDIA 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994071"
---
# <a name="disablemedia-property"></a>DISABLEMEDIA 屬性

設定 [**DISABLEMEDIA**](disablemedia.md) 屬性可防止安裝程式將任何媒體來源（例如 cd-rom）註冊為產品的有效來源。 但是，如果已啟用流覽，使用者仍可流覽至媒體來源。

## <a name="remarks"></a>備註

請注意， [**DISABLEMEDIA**](disablemedia.md) 屬性與設定 DISABLEMEDIA 原則的效果不同。 設定 **DISABLEMEDIA** 可防止註冊任何媒體來源，這也會防止第一次從媒體來源安裝應用程式。

如需保護 [*受管理應用程式*](m-gly.md) 的媒體來源以避免由非系統管理使用者進行流覽和安裝的詳細資訊，請參閱 [來源復原](source-resiliency.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




