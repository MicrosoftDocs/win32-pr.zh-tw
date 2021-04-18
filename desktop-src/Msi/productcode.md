---
description: '[ProductCode] 屬性是特定產品版本的唯一識別碼，以字串 GUID 表示，例如 &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;。'
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976169"
---
# <a name="productcode-property"></a>ProductCode 屬性

[ **ProductCode** ] 屬性是特定產品版本的唯一識別碼，以字串 [GUID](guid.md)表示，例如 " {12345678-1234-1234-1234-123456789012} "。 此 GUID 中使用的字母必須為大寫。 此識別碼必須因不同版本和語言而有所不同。

將產品更新為全新產品的產品升級，也必須變更產品代碼。 應用程式套件的32位和64位版本必須獲派不同的產品代碼。

**ProductCode** 會公告為 product 屬性，而且是指定產品的主要方法。 此為必要屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




