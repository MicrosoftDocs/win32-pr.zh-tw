---
description: MsiHiddenProperties 屬性可用來防止安裝程式在記錄檔中顯示密碼或其他機密資訊。
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: MsiHiddenProperties 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000455"
---
# <a name="msihiddenproperties-property"></a>MsiHiddenProperties 屬性

**MsiHiddenProperties** 屬性可用來防止安裝程式在記錄檔中顯示密碼或其他機密資訊。 若要防止將屬性寫入記錄檔，請將 **MsiHiddenProperties** 屬性的值設定為您想要隱藏的屬性名稱。 您可以藉由指定以分號分隔的屬性名稱字串 (; ) 來隱藏多個屬性。

> [!Note]  
> 當 [調試](debug.md) 程式原則設定為7的值時，安裝程式會將命令列上輸入的資訊寫入記錄檔中。 如此，即使屬性包含在 **MsiHiddenProperties** 屬性中，也會顯示在命令列上輸入的公用屬性。 這可讓您在記錄檔中顯示的命令列上輸入機密資訊。 如需詳細資訊，請參閱 [防止機密資訊寫入至記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




