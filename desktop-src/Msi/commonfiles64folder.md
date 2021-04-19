---
description: 安裝程式會將 CommonFiles64Folder 屬性設定為預先定義的64位通用檔案資料夾的完整路徑。 現有的 CommonFilesFolder 屬性會設定為對應的32位資料夾。
ms.assetid: 6730170a-0f73-4a84-b3fb-bd15c72917c7
title: CommonFiles64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44a6720e609cfa79cd0e4adbfd5136c7a92a5ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993369"
---
# <a name="commonfiles64folder-property"></a><span data-ttu-id="e9808-104">CommonFiles64Folder 屬性</span><span class="sxs-lookup"><span data-stu-id="e9808-104">CommonFiles64Folder property</span></span>

<span data-ttu-id="e9808-105">安裝程式會將 **CommonFiles64Folder** 屬性設定為預先定義的64位通用檔案資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e9808-105">The installer sets the **CommonFiles64Folder** property to the full path of the predefined 64-bit Common Files folder.</span></span> <span data-ttu-id="e9808-106">現有的 [**CommonFilesFolder**](commonfilesfolder.md) 屬性會設定為對應的32位資料夾。</span><span class="sxs-lookup"><span data-stu-id="e9808-106">The existing [**CommonFilesFolder**](commonfilesfolder.md) property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9808-107">備註</span><span class="sxs-lookup"><span data-stu-id="e9808-107">Remarks</span></span>

<span data-ttu-id="e9808-108">安裝程式會在64位 Windows 上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e9808-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="e9808-109">這個屬性不會用於32位的 Windows 上。</span><span class="sxs-lookup"><span data-stu-id="e9808-109">This property is not used on 32-bit Windows.</span></span> <span data-ttu-id="e9808-110">使用64位 Windows 時，此值可能是 "C： \\ Program files \\ Common Files"。</span><span class="sxs-lookup"><span data-stu-id="e9808-110">When using 64-bit Windows, the value may be "C:\\Program Files\\Common Files".</span></span>

## <a name="requirements"></a><span data-ttu-id="e9808-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9808-111">Requirements</span></span>



| <span data-ttu-id="e9808-112">需求</span><span class="sxs-lookup"><span data-stu-id="e9808-112">Requirement</span></span> | <span data-ttu-id="e9808-113">值</span><span class="sxs-lookup"><span data-stu-id="e9808-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9808-114">版本</span><span class="sxs-lookup"><span data-stu-id="e9808-114">Version</span></span><br/> | <span data-ttu-id="e9808-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e9808-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e9808-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e9808-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e9808-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="e9808-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e9808-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="e9808-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9808-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9808-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9808-120">屬性</span><span class="sxs-lookup"><span data-stu-id="e9808-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




