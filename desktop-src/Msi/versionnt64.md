---
description: 只有當系統正在64位的電腦上執行時，安裝程式才會將 VersionNT64 屬性設定為作業系統的版本號碼。
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998771"
---
# <a name="versionnt64-property"></a><span data-ttu-id="4e7c5-103">VersionNT64 屬性</span><span class="sxs-lookup"><span data-stu-id="4e7c5-103">VersionNT64 property</span></span>

<span data-ttu-id="4e7c5-104">只有當系統正在64位的電腦上執行時，安裝程式才會將 **VersionNT64** 屬性設定為作業系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="4e7c5-105">如果作業系統不是64位，則屬性是未定義的。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="4e7c5-106">此值為整數： MajorVersion \* 100 + MinorVersion。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="4e7c5-107">基於相容性的理由，如果 [**範本摘要**](template-summary.md) 內容指出封裝適用于32位 Intel 系統，且作業系統是不是 Intel64 或 x64 (的64位架構（例如 ARM64) ），則屬性也是未定義的。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel systems and the operating system is a 64-bit architecture that is not Intel64 or x64 (such as ARM64).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7c5-108">備註</span><span class="sxs-lookup"><span data-stu-id="4e7c5-108">Remarks</span></span>

<span data-ttu-id="4e7c5-109">條件運算式會測試64位 Windows，只要使用屬性名稱，或是使用比較運算子來驗證版本。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-109">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7c5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e7c5-110">Requirements</span></span>



| <span data-ttu-id="4e7c5-111">需求</span><span class="sxs-lookup"><span data-stu-id="4e7c5-111">Requirement</span></span> | <span data-ttu-id="4e7c5-112">值</span><span class="sxs-lookup"><span data-stu-id="4e7c5-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7c5-113">版本</span><span class="sxs-lookup"><span data-stu-id="4e7c5-113">Version</span></span><br/> | <span data-ttu-id="4e7c5-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4e7c5-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4e7c5-116">Windows Installer 在 Windows Server 2003 或 Windows XP 上，請參閱 Windows Installer Run-Time Windows Installer 版本所需的最低 Windows service pack 相關資訊的 [需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="4e7c5-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e7c5-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e7c5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7c5-118">屬性</span><span class="sxs-lookup"><span data-stu-id="4e7c5-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




