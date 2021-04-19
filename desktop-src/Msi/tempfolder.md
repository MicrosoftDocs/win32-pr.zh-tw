---
description: 安裝程式會將 TempFolder 屬性設定為 Temp 資料夾的完整路徑。作者應該不需要設定 TempFolder 屬性。
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: TempFolder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999106"
---
# <a name="tempfolder-property"></a><span data-ttu-id="a1013-103">TempFolder 屬性</span><span class="sxs-lookup"><span data-stu-id="a1013-103">TempFolder property</span></span>

<span data-ttu-id="a1013-104">安裝程式會將 **TempFolder** 屬性設定為 Temp 資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a1013-104">The installer sets the **TempFolder** property to the full path to the Temp folder.</span></span>

<span data-ttu-id="a1013-105">作者應該不需要設定 **TempFolder** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a1013-105">Authors should not need to set the **TempFolder** property.</span></span> <span data-ttu-id="a1013-106">Windows Installer 使用 [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) 函式來取出為暫存檔案指定的目錄路徑，並設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a1013-106">Windows Installer uses the [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files and to set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1013-107">備註</span><span class="sxs-lookup"><span data-stu-id="a1013-107">Remarks</span></span>

<span data-ttu-id="a1013-108">這個屬性的通用值為 C： \\ Temp。</span><span class="sxs-lookup"><span data-stu-id="a1013-108">A common value for this property is C:\\Temp.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1013-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1013-109">Requirements</span></span>



| <span data-ttu-id="a1013-110">需求</span><span class="sxs-lookup"><span data-stu-id="a1013-110">Requirement</span></span> | <span data-ttu-id="a1013-111">值</span><span class="sxs-lookup"><span data-stu-id="a1013-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1013-112">版本</span><span class="sxs-lookup"><span data-stu-id="a1013-112">Version</span></span><br/> | <span data-ttu-id="a1013-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a1013-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a1013-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a1013-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a1013-115">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="a1013-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a1013-116">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="a1013-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1013-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1013-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1013-118">屬性</span><span class="sxs-lookup"><span data-stu-id="a1013-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 
