---
description: 安裝程式物件的環境屬性是讀寫屬性，它是目前進程之環境變數的字串值。
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: 安裝程式. 環境屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975745"
---
# <a name="installerenvironment-property"></a><span data-ttu-id="fd096-103">安裝程式. 環境屬性</span><span class="sxs-lookup"><span data-stu-id="fd096-103">Installer.Environment property</span></span>

<span data-ttu-id="fd096-104">[**安裝程式**](installer-object.md)物件的 **環境** 屬性是讀寫屬性，它是目前進程之環境變數的字串值。</span><span class="sxs-lookup"><span data-stu-id="fd096-104">The **Environment** property of the [**Installer**](installer-object.md) object is a read-write property that is the string value for an environment variable of the current process.</span></span>

<span data-ttu-id="fd096-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd096-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd096-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd096-106">Syntax</span></span>


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a><span data-ttu-id="fd096-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="fd096-107">Property value</span></span>

<span data-ttu-id="fd096-108">要讀取或寫入的環境變數名稱。</span><span class="sxs-lookup"><span data-stu-id="fd096-108">The name of the environment variable to be read or written.</span></span> <span data-ttu-id="fd096-109">這不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="fd096-109">This is case-insensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd096-110">備註</span><span class="sxs-lookup"><span data-stu-id="fd096-110">Remarks</span></span>

<span data-ttu-id="fd096-111">使用 **環境** 屬性設定環境變數只會影響作用中的會話。</span><span class="sxs-lookup"><span data-stu-id="fd096-111">Setting an environment variable with the **Environment** property only affects the active session.</span></span> <span data-ttu-id="fd096-112">若要對環境變數進行持續變更，請使用 [環境資料表](environment-table.md)。</span><span class="sxs-lookup"><span data-stu-id="fd096-112">To make persistent changes to an environment variable, use the [Environment table](environment-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd096-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd096-113">Requirements</span></span>



| <span data-ttu-id="fd096-114">需求</span><span class="sxs-lookup"><span data-stu-id="fd096-114">Requirement</span></span> | <span data-ttu-id="fd096-115">值</span><span class="sxs-lookup"><span data-stu-id="fd096-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd096-116">版本</span><span class="sxs-lookup"><span data-stu-id="fd096-116">Version</span></span><br/> | <span data-ttu-id="fd096-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="fd096-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fd096-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="fd096-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fd096-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fd096-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fd096-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fd096-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd096-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd096-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fd096-122">IID</span><span class="sxs-lookup"><span data-stu-id="fd096-122">IID</span></span><br/>     | <span data-ttu-id="fd096-123">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fd096-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




