---
description: FormattedSDDLText 資料類型的資料庫欄位保存文字字串，該字串會使用有效的安全描述項定義語言 (SDDL 來描述安全描述項。 ) 此資料類型是由 MsiLockPermissionsEx 資料表的 SDDLText 欄位使用，以保護選取的物件。 請注意，MsiLockPermissionsEx 資料表的 SDDLText 欄位不支援私用或公用屬性。
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ddfeac55f05ebea5f1603def6adcbac32aa9d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992431"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

**FormattedSDDLText** 資料類型的資料庫欄位保存文字字串，該字串會使用有效的 [安全描述項定義語言](../secauthz/security-descriptor-definition-language.md) (SDDL 來描述安全描述項。 ) 此資料類型是由 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md)的 SDDLText 欄位使用，以保護選取的物件。 請注意，MsiLockPermissionsEx 資料表的 SDDLText 欄位不支援私用或公用屬性。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用此資料類型。

**FormattedSDDLText** 資料類型可以保存以有效 [安全描述項字串格式](../secauthz/security-descriptor-string-format.md)撰寫的 SDDL 字串。 如需有關 SDDL 的詳細資訊，請參閱[Microsoft Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)的[存取控制](../secauthz/access-control.md)一節。 此外， **FormattedSDDLText** 的文字字串可以使用角括弧 (<>) 包含要決定其帳戶 SID 之使用者的網域和使用者名稱。

如果使用者名稱為 *SampleUser* 的使用者屬於名為 *SampleDomain* 的網域，則 **FormattedSDDLText** 值可以使用 SID 字串、使用者名稱和功能變數名稱，或 Windows 環境變數來識別擁有者。 例如，可能會有下列字串。

<dl> O：*owner \_ sid \_ string* G:BAD： (D; OICI; GA;;;BG)  (A; OICI; GRGWGX;;;*擁有者 \_ sid \_ 字串*)  (A; OICI; GA;;;BA) S:ARAI (AU;SAFA; FA;;;WD)   
O： <*SampleDomain \\ SAMPLEUSER*>G:BAD： (D; OICI; GA;;;BG)  (A; OICI; GRGWGX;;;<*SampleDomain \\ SampleUser*>)  (A; OICI; GA;;;BA) S:ARAI (AU;SAFA; FA;;;WD)   
O： <\[ % USERDOMAIN \] \\ \[ % USERNAME \]>G:BAD： (D; OICI; GA;;;BG)  (A; OICI; GRGWGX;;;<\[ % USERDOMAIN \] \\ \[ % USERNAME \]>)  (A; OICI; GA;;;BA) S:ARAI (AU;SAFA; FA;;;WD) 
</dl>

 

 
