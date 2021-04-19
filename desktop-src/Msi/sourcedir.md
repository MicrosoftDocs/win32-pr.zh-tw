---
description: SourceDir 屬性是包含來源封包檔的根目錄，或是安裝套件的來源檔案樹狀目錄。 此值用於目錄解析。
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001186"
---
# <a name="sourcedir-property"></a>SourceDir 屬性

**SourceDir** 屬性是包含來源封包檔的根目錄，或是安裝套件的來源檔案樹狀目錄。 此值用於目錄解析。

## <a name="default-value"></a>預設值

包含安裝套件的目錄。

## <a name="remarks"></a>備註

在任何運算式中使用 **SourceDir** 屬性，或嘗試使用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)取得 **SourceDir** 的值之前，必須先呼叫 [ResolveSource 動作](resolvesource-action.md)。 無法在來源無法使用時執行 ResolveSource 動作，例如在卸載應用程式時，因為這可能會導致來源媒體出現非預期的提示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




