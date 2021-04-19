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
# <a name="msihiddenproperties-property"></a><span data-ttu-id="e8f07-103">MsiHiddenProperties 屬性</span><span class="sxs-lookup"><span data-stu-id="e8f07-103">MsiHiddenProperties property</span></span>

<span data-ttu-id="e8f07-104">**MsiHiddenProperties** 屬性可用來防止安裝程式在記錄檔中顯示密碼或其他機密資訊。</span><span class="sxs-lookup"><span data-stu-id="e8f07-104">The **MsiHiddenProperties** property may be used to prevent the installer from displaying passwords or other confidential information in the log file.</span></span> <span data-ttu-id="e8f07-105">若要防止將屬性寫入記錄檔，請將 **MsiHiddenProperties** 屬性的值設定為您想要隱藏的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f07-105">To prevent a property from being written into the log file, set the value of the **MsiHiddenProperties** property to the name of the property you wish to hide.</span></span> <span data-ttu-id="e8f07-106">您可以藉由指定以分號分隔的屬性名稱字串 (; ) 來隱藏多個屬性。</span><span class="sxs-lookup"><span data-stu-id="e8f07-106">You can hide multiple properties by specifying a string of property names delimited by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="e8f07-107">當 [調試](debug.md) 程式原則設定為7的值時，安裝程式會將命令列上輸入的資訊寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="e8f07-107">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="e8f07-108">如此，即使屬性包含在 **MsiHiddenProperties** 屬性中，也會顯示在命令列上輸入的公用屬性。</span><span class="sxs-lookup"><span data-stu-id="e8f07-108">This makes public properties entered on a command line visible even if the property is included in the **MsiHiddenProperties** property.</span></span> <span data-ttu-id="e8f07-109">這可讓您在記錄檔中顯示的命令列上輸入機密資訊。</span><span class="sxs-lookup"><span data-stu-id="e8f07-109">This can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="e8f07-110">如需詳細資訊，請參閱 [防止機密資訊寫入至記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="e8f07-110">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8f07-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8f07-111">Requirements</span></span>



| <span data-ttu-id="e8f07-112">需求</span><span class="sxs-lookup"><span data-stu-id="e8f07-112">Requirement</span></span> | <span data-ttu-id="e8f07-113">值</span><span class="sxs-lookup"><span data-stu-id="e8f07-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f07-114">版本</span><span class="sxs-lookup"><span data-stu-id="e8f07-114">Version</span></span><br/> | <span data-ttu-id="e8f07-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e8f07-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e8f07-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e8f07-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e8f07-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="e8f07-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e8f07-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="e8f07-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8f07-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8f07-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f07-120">屬性</span><span class="sxs-lookup"><span data-stu-id="e8f07-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




