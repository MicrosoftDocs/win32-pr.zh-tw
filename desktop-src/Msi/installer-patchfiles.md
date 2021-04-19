---
description: PatchFiles 屬性會傳回 StringList 物件，其中包含可由提供的修補程式清單更新的檔案清單。
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: PatchFiles 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981663"
---
# <a name="installerpatchfiles-property"></a>PatchFiles 屬性

**PatchFiles** 屬性會傳回 [**StringList**](stringlist-object.md)物件，其中包含可由提供的修補程式清單更新的檔案清單。 這個屬性會呼叫 [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)。 如需使用 **PatchFiles** 屬性的詳細資訊，請參閱 [列出可更新的](listing-the-files-that-can-be-updated.md)檔案。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**安裝程式物件**](installer-object.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




