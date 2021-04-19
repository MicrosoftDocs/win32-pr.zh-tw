---
description: 設定 SHORTFILENAMES 屬性會導致將短檔案名用於目標檔案的名稱，而不是完整的檔案名。 它不會影響安裝程式在來源尋找的檔案名。
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: SHORTFILENAMES 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980239"
---
# <a name="shortfilenames-property"></a><span data-ttu-id="b0b02-104">SHORTFILENAMES 屬性</span><span class="sxs-lookup"><span data-stu-id="b0b02-104">SHORTFILENAMES property</span></span>

<span data-ttu-id="b0b02-105">設定 **SHORTFILENAMES** 屬性會導致將短檔案名用於目標檔案的名稱，而不是完整的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b0b02-105">Setting the **SHORTFILENAMES** property causes short file names to be used for the names of target files, rather than long file names.</span></span> <span data-ttu-id="b0b02-106">它不會影響安裝程式在來源尋找的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b0b02-106">It does not affect the file names the installer looks for at the source.</span></span>

## <a name="default-value"></a><span data-ttu-id="b0b02-107">預設值</span><span class="sxs-lookup"><span data-stu-id="b0b02-107">Default Value</span></span>

<span data-ttu-id="b0b02-108">如果未設定 **SHORTFILENAMES** 屬性，而且目標磁片區支援長名稱，則安裝程式會使用完整名稱。</span><span class="sxs-lookup"><span data-stu-id="b0b02-108">Long names are used by the installer if the **SHORTFILENAMES** property is not set and the target volume supports long names.</span></span> <span data-ttu-id="b0b02-109">如果目標磁片區不支援長名稱，則安裝程式會使用簡短名稱。</span><span class="sxs-lookup"><span data-stu-id="b0b02-109">Short names are used by the installer if the target volume does not support long names.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b02-110">備註</span><span class="sxs-lookup"><span data-stu-id="b0b02-110">Remarks</span></span>

<span data-ttu-id="b0b02-111">當設定 **SHORTFILENAMES** 屬性時，安裝程式會使用檔案 \| [資料表](file-table.md) 或 [目錄資料表](directory-table.md)中所列之任何短組的簡短檔案名，建立資料夾並安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="b0b02-111">When the **SHORTFILENAMES** property is set, the installer creates folders and installs files using short file names from any short\|long pairs listed in the [File table](file-table.md) or [Directory table](directory-table.md).</span></span>

<span data-ttu-id="b0b02-112">應用程式可以使用 [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) 函式來取出指定檔案路徑的簡短路徑形式。</span><span class="sxs-lookup"><span data-stu-id="b0b02-112">Applications can use the [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) function to retrieve the short path form of a specified file path.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b02-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0b02-113">Requirements</span></span>



| <span data-ttu-id="b0b02-114">需求</span><span class="sxs-lookup"><span data-stu-id="b0b02-114">Requirement</span></span> | <span data-ttu-id="b0b02-115">值</span><span class="sxs-lookup"><span data-stu-id="b0b02-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b02-116">版本</span><span class="sxs-lookup"><span data-stu-id="b0b02-116">Version</span></span><br/> | <span data-ttu-id="b0b02-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="b0b02-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b0b02-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="b0b02-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b0b02-119">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="b0b02-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b0b02-120">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="b0b02-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0b02-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0b02-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b02-122">屬性</span><span class="sxs-lookup"><span data-stu-id="b0b02-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 
