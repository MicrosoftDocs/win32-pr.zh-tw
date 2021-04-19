---
description: 設定 DISABLEADVTSHORTCUTS 屬性時，會停用產生支援隨選安裝和公告的快捷方式。 設定這個屬性會指定這些快速鍵應該改由一般快速鍵取代。
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: DISABLEADVTSHORTCUTS 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981090"
---
# <a name="disableadvtshortcuts-property"></a><span data-ttu-id="957f8-104">DISABLEADVTSHORTCUTS 屬性</span><span class="sxs-lookup"><span data-stu-id="957f8-104">DISABLEADVTSHORTCUTS property</span></span>

<span data-ttu-id="957f8-105">設定 **DISABLEADVTSHORTCUTS** 屬性時，會停用產生支援 [隨選安裝](installation-on-demand.md) 和 [公告](advertisement.md)的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="957f8-105">Setting the **DISABLEADVTSHORTCUTS** property disables the generation of shortcuts supporting [installation-on-demand](installation-on-demand.md) and [advertisement](advertisement.md).</span></span> <span data-ttu-id="957f8-106">設定這個屬性會指定這些快速鍵應該改由一般快速鍵取代。</span><span class="sxs-lookup"><span data-stu-id="957f8-106">Setting this property specifies that these shortcuts should instead be replaced by regular shortcuts.</span></span>

## <a name="default-value"></a><span data-ttu-id="957f8-107">預設值</span><span class="sxs-lookup"><span data-stu-id="957f8-107">Default Value</span></span>

<span data-ttu-id="957f8-108">依預設，會啟用隨選安裝的快捷方式產生。</span><span class="sxs-lookup"><span data-stu-id="957f8-108">By default, installation-on-demand shortcut generation is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="957f8-109">備註</span><span class="sxs-lookup"><span data-stu-id="957f8-109">Remarks</span></span>

<span data-ttu-id="957f8-110">支援廣告的快速鍵具有功能的名稱，而不是在 \[ \# \] [快捷方式資料表](shortcut-table.md)的目標資料行中輸入的 filekey 格式檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="957f8-110">The shortcuts that support advertisement have the name of a feature, rather than a formatted file path of the form \[\#filekey\], entered in the Target column of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="957f8-111">如果已設定此屬性，且已安裝此功能，安裝程式會產生一般功能的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="957f8-111">If this property is set and the feature is installed, the installer generates a regular shortcut to the feature.</span></span>

<span data-ttu-id="957f8-112">系統管理員通常會使用這個屬性，讓使用者在不支援廣告的環境之間漫遊。</span><span class="sxs-lookup"><span data-stu-id="957f8-112">This property is commonly used by administrators for users who roam between environments that do and do not support advertising.</span></span> <span data-ttu-id="957f8-113">這個屬性可由轉換、系統管理資料流程或 [屬性工作表](property-table.md)中的設定來設定。</span><span class="sxs-lookup"><span data-stu-id="957f8-113">This property can be set by a transform, in the administrative stream, or in the [Property table](property-table.md).</span></span> <span data-ttu-id="957f8-114">如果是使用命令列或呼叫 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)來設定，則必須在每次後續安裝期間再次重設。</span><span class="sxs-lookup"><span data-stu-id="957f8-114">If it is set using the command line or by a call to [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), then it must be reset again during each subsequent installation.</span></span>

## <a name="requirements"></a><span data-ttu-id="957f8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="957f8-115">Requirements</span></span>



| <span data-ttu-id="957f8-116">需求</span><span class="sxs-lookup"><span data-stu-id="957f8-116">Requirement</span></span> | <span data-ttu-id="957f8-117">值</span><span class="sxs-lookup"><span data-stu-id="957f8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="957f8-118">版本</span><span class="sxs-lookup"><span data-stu-id="957f8-118">Version</span></span><br/> | <span data-ttu-id="957f8-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="957f8-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="957f8-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="957f8-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="957f8-121">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="957f8-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="957f8-122">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="957f8-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="957f8-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="957f8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957f8-124">屬性</span><span class="sxs-lookup"><span data-stu-id="957f8-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




