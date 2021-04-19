---
description: 安裝程式物件的 Version 屬性是唯讀屬性，它是目前版本 Windows Installer 的字串表示。 字串會以下列格式傳回。
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: 安裝程式版本屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980195"
---
# <a name="installerversion-property"></a><span data-ttu-id="abea5-104">安裝程式版本屬性</span><span class="sxs-lookup"><span data-stu-id="abea5-104">Installer.Version property</span></span>

<span data-ttu-id="abea5-105">[**安裝程式**](installer-object.md)物件的 **Version** 屬性是唯讀屬性，它是目前版本 Windows Installer 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="abea5-105">The **Version** property of the [**Installer**](installer-object.md) object is a read-only property that is the string representation of the current version of Windows Installer.</span></span> <span data-ttu-id="abea5-106">字串會以下列格式傳回。</span><span class="sxs-lookup"><span data-stu-id="abea5-106">The string is returned in the following form.</span></span>

<span data-ttu-id="abea5-107">*主要*。*次要*。*build*。*更新*</span><span class="sxs-lookup"><span data-stu-id="abea5-107">*major*.*minor*.*build*.*update*</span></span>

<span data-ttu-id="abea5-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="abea5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="abea5-109">語法</span><span class="sxs-lookup"><span data-stu-id="abea5-109">Syntax</span></span>


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a><span data-ttu-id="abea5-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="abea5-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="abea5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="abea5-111">Requirements</span></span>



| <span data-ttu-id="abea5-112">需求</span><span class="sxs-lookup"><span data-stu-id="abea5-112">Requirement</span></span> | <span data-ttu-id="abea5-113">值</span><span class="sxs-lookup"><span data-stu-id="abea5-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abea5-114">版本</span><span class="sxs-lookup"><span data-stu-id="abea5-114">Version</span></span><br/> | <span data-ttu-id="abea5-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="abea5-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="abea5-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="abea5-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="abea5-117">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="abea5-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="abea5-118">DLL</span><span class="sxs-lookup"><span data-stu-id="abea5-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="abea5-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abea5-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="abea5-120">IID</span><span class="sxs-lookup"><span data-stu-id="abea5-120">IID</span></span><br/>     | <span data-ttu-id="abea5-121">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="abea5-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




