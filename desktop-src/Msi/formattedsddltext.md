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
# <a name="formattedsddltext"></a><span data-ttu-id="51971-104">FormattedSDDLText</span><span class="sxs-lookup"><span data-stu-id="51971-104">FormattedSDDLText</span></span>

<span data-ttu-id="51971-105">**FormattedSDDLText** 資料類型的資料庫欄位保存文字字串，該字串會使用有效的 [安全描述項定義語言](../secauthz/security-descriptor-definition-language.md) (SDDL 來描述安全描述項。 ) 此資料類型是由 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md)的 SDDLText 欄位使用，以保護選取的物件。</span><span class="sxs-lookup"><span data-stu-id="51971-105">A database field of the **FormattedSDDLText** data type holds a text string that describes a security descriptor using valid [security descriptor definition language](../secauthz/security-descriptor-definition-language.md) (SDDL.) This data type is used by the SDDLText field of the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) to secure a selected object.</span></span> <span data-ttu-id="51971-106">請注意，MsiLockPermissionsEx 資料表的 SDDLText 欄位不支援私用或公用屬性。</span><span class="sxs-lookup"><span data-stu-id="51971-106">Note that the SDDLText field of the MsiLockPermissionsEx Table does not support private or public properties.</span></span>

<span data-ttu-id="51971-107">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="51971-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="51971-108">從 Windows Installer 5.0 開始，可以使用此資料類型。</span><span class="sxs-lookup"><span data-stu-id="51971-108">This data type is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="51971-109">**FormattedSDDLText** 資料類型可以保存以有效 [安全描述項字串格式](../secauthz/security-descriptor-string-format.md)撰寫的 SDDL 字串。</span><span class="sxs-lookup"><span data-stu-id="51971-109">The **FormattedSDDLText** data type can hold a SDDL string written in valid [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span> <span data-ttu-id="51971-110">如需有關 SDDL 的詳細資訊，請參閱[Microsoft Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)的[存取控制](../secauthz/access-control.md)一節。</span><span class="sxs-lookup"><span data-stu-id="51971-110">For more information about SDDL, see the [Access Control](../secauthz/access-control.md) section of the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).</span></span> <span data-ttu-id="51971-111">此外， **FormattedSDDLText** 的文字字串可以使用角括弧 (<>) 包含要決定其帳戶 SID 之使用者的網域和使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="51971-111">In addition, a **FormattedSDDLText** text string can use angle brackets (<>) to contain the domain and user name of the user whose account SID is to be determined.</span></span>

<span data-ttu-id="51971-112">如果使用者名稱為 *SampleUser* 的使用者屬於名為 *SampleDomain* 的網域，則 **FormattedSDDLText** 值可以使用 SID 字串、使用者名稱和功能變數名稱，或 Windows 環境變數來識別擁有者。</span><span class="sxs-lookup"><span data-stu-id="51971-112">If the user having user name *SampleUser* belongs to a domain named *SampleDomain*, then the **FormattedSDDLText** value can identify the owner using the SID string, the user name and domain name, or the Windows environment variables.</span></span> <span data-ttu-id="51971-113">例如，可能會有下列字串。</span><span class="sxs-lookup"><span data-stu-id="51971-113">For example, the following strings would be possible.</span></span>

<dl> <span data-ttu-id="51971-114">O：*owner \_ sid \_ string* G:BAD： (D; OICI; GA;;;BG)  (A; OICI; GRGWGX;;;*擁有者 \_ sid \_ 字串*)  (A; OICI; GA;;;BA) S:ARAI (AU;SAFA; FA;;;WD) </span><span class="sxs-lookup"><span data-stu-id="51971-114">O:*owner\_sid\_string* G:BAD:(D;OICI;GA;;;BG)(A;OICI;GRGWGX;;;*owner\_sid\_string*)(A;OICI;GA;;;BA)S:ARAI(AU;SAFA;FA;;;WD)</span></span>  
<span data-ttu-id="51971-115">O： <*SampleDomain \\ SAMPLEUSER*>G:BAD： (D; OICI; GA;;;BG)  (A; OICI; GRGWGX;;;<*SampleDomain \\ SampleUser*>)  (A; OICI; GA;;;BA) S:ARAI (AU;SAFA; FA;;;WD) </span><span class="sxs-lookup"><span data-stu-id="51971-115">O:<*SampleDomain\\SampleUser*>G:BAD:(D;OICI;GA;;;BG)(A;OICI;GRGWGX;;;<*SampleDomain\\SampleUser*>)(A;OICI;GA;;;BA)S:ARAI(AU;SAFA;FA;;;WD)</span></span>  
<span data-ttu-id="51971-116">O： <\[ % USERDOMAIN \] \\ \[ % USERNAME \]>G:BAD： (D; OICI; GA;;;BG)  (A; OICI; GRGWGX;;;<\[ % USERDOMAIN \] \\ \[ % USERNAME \]>)  (A; OICI; GA;;;BA) S:ARAI (AU;SAFA; FA;;;WD) </span><span class="sxs-lookup"><span data-stu-id="51971-116">O:<\[%USERDOMAIN\]\\\[%USERNAME\]>G:BAD:(D;OICI;GA;;;BG)(A;OICI;GRGWGX;;;<\[%USERDOMAIN\]\\\[%USERNAME\]>)(A;OICI;GA;;;BA)S:ARAI(AU;SAFA;FA;;;WD)</span></span>
</dl>

 

 
