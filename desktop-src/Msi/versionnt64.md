---
description: 只有當系統正在64位的電腦上執行時，安裝程式才會將 VersionNT64 屬性設定為作業系統的版本號碼。
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262070"
---
# <a name="versionnt64-property"></a><span data-ttu-id="750f4-103">VersionNT64 屬性</span><span class="sxs-lookup"><span data-stu-id="750f4-103">VersionNT64 property</span></span>

<span data-ttu-id="750f4-104">只有當系統正在64位的電腦上執行時，安裝程式才會將 **VersionNT64** 屬性設定為作業系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="750f4-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="750f4-105">如果作業系統不是64位，則屬性是未定義的。</span><span class="sxs-lookup"><span data-stu-id="750f4-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="750f4-106">此值為整數： MajorVersion \* 100 + MinorVersion。</span><span class="sxs-lookup"><span data-stu-id="750f4-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="750f4-107">基於相容性的理由，如果 [**範本摘要**](template-summary.md) 內容指出封裝適用于32位 intel (x86) 系統，且作業系統無法執行64位 intel (x64) 程式碼（例如 ARM Windows 10 ARM64 (上的) ），則屬性也是未定義的。</span><span class="sxs-lookup"><span data-stu-id="750f4-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel (x86) systems and the operating system cannot run 64-bit Intel (x64) code, such as Windows 10 on ARM (ARM64).</span></span>

> [!NOTE]
> <span data-ttu-id="750f4-108">從 Windows 10 組建21277，Windows Insider Preview 計畫的開發人員通道中的 ARM64 組建支援 x64 應用程式。</span><span class="sxs-lookup"><span data-stu-id="750f4-108">As of Windows 10 Build 21277, ARM64 builds in the Dev channel of the Windows Insider Preview program have support for x64 applications.</span></span> <span data-ttu-id="750f4-109">在這些 ARM64 組建中，會針對 x86 套件定義 VersionNT64 屬性。</span><span class="sxs-lookup"><span data-stu-id="750f4-109">On these ARM64 builds, the VersionNT64 property is defined for x86 packages.</span></span>

## <a name="remarks"></a><span data-ttu-id="750f4-110">備註</span><span class="sxs-lookup"><span data-stu-id="750f4-110">Remarks</span></span>

<span data-ttu-id="750f4-111">條件運算式會測試64位 Windows，只要使用屬性名稱，或是使用比較運算子來驗證版本。</span><span class="sxs-lookup"><span data-stu-id="750f4-111">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="750f4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="750f4-112">Requirements</span></span>



| <span data-ttu-id="750f4-113">需求</span><span class="sxs-lookup"><span data-stu-id="750f4-113">Requirement</span></span> | <span data-ttu-id="750f4-114">值</span><span class="sxs-lookup"><span data-stu-id="750f4-114">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="750f4-115">版本</span><span class="sxs-lookup"><span data-stu-id="750f4-115">Version</span></span><br/> | <span data-ttu-id="750f4-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="750f4-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="750f4-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="750f4-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="750f4-118">Windows Installer 在 Windows Server 2003 或 Windows XP 上，請參閱 Windows Installer Run-Time Windows Installer 版本所需的最低 Windows service pack 相關資訊的 [需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="750f4-118">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="750f4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="750f4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750f4-120">屬性</span><span class="sxs-lookup"><span data-stu-id="750f4-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




