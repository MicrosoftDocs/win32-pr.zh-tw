---
description: 安裝程式會將 UserSID 屬性的值設定為執行安裝之使用者的安全識別碼 (SID) 的字串表示。 如需詳細資訊，請參閱授權結構。
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990233"
---
# <a name="usersid-property"></a>UserSID 屬性

安裝程式會將 **UserSID** 屬性的值設定為執行安裝之使用者的安全識別碼 (SID) 的字串表示。 如需詳細資訊，請參閱 [授權結構](../secauthz/authorization-structures.md)。

## <a name="default-value"></a>預設值

無。

## <a name="remarks"></a>備註

Windows Installer 在 Windows 2000、Windows XP 和 Windows Vista 上設定此屬性。 這個屬性未在所有其他作業系統上定義。

請注意，這個屬性具有可從延遲的自訂動作中取出的特殊屬性。 以較高許可權執行的自訂動作仍然可以在 **UserSID** 屬性中傳回使用者的 SID。 如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
