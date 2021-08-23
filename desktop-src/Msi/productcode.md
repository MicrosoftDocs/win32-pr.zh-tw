---
description: '[ProductCode] 屬性是特定產品版本的唯一識別碼，以字串 GUID 表示，例如 &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;。'
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a77ba270075b214d5eee2ee804c6849a2ef71561610ee60ae3eb4941e43465c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753908"
---
# <a name="productcode-property"></a>ProductCode 屬性

[ **ProductCode** ] 屬性是特定產品版本的唯一識別碼，以字串 [GUID](guid.md)表示，例如 " {12345678-1234-1234-1234-123456789012} "。 此 GUID 中使用的字母必須為大寫。 此識別碼必須因不同版本和語言而有所不同。

將產品更新為全新產品的產品升級，也必須變更產品代碼。 應用程式套件的32位和64位版本必須獲派不同的產品代碼。

**ProductCode** 會公告為 product 屬性，而且是指定產品的主要方法。 此為必要屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




