---
description: 安裝程式會將 UserSID 屬性的值設定為執行安裝之使用者的安全識別碼 (SID) 的字串表示。 如需詳細資訊，請參閱授權結構。
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26185c886117b39355241151ffef6d8615bd5f8d10a7f50bd5937a301f7b398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809158"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
