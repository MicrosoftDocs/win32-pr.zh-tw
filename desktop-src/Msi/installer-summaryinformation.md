---
description: 安裝程式物件的 SummaryInformation 屬性會傳回 SummaryInfo 物件，此物件可用來檢查、更新和加入屬性至封裝或轉換的摘要資訊資料流程中。
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: SummaryInformation 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983973"
---
# <a name="installersummaryinformation-property"></a><span data-ttu-id="5c8bd-103">SummaryInformation 屬性</span><span class="sxs-lookup"><span data-stu-id="5c8bd-103">Installer.SummaryInformation property</span></span>

<span data-ttu-id="5c8bd-104">[**安裝程式**](installer-object.md)物件的 **SummaryInformation** 屬性會傳回 [**SummaryInfo**](summaryinfo-object.md)物件，此物件可用來檢查、更新和加入屬性至封裝或轉換的摘要資訊資料流程中。</span><span class="sxs-lookup"><span data-stu-id="5c8bd-104">The **SummaryInformation** property of the [**Installer**](installer-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream of a package or transform.</span></span>

<span data-ttu-id="5c8bd-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5c8bd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8bd-106">語法</span><span class="sxs-lookup"><span data-stu-id="5c8bd-106">Syntax</span></span>


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="5c8bd-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="5c8bd-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8bd-108">備註</span><span class="sxs-lookup"><span data-stu-id="5c8bd-108">Remarks</span></span>

<span data-ttu-id="5c8bd-109">如果使用大於0的 *maxProperties* 值來開啟現有的摘要資訊資料流程，就必須在關閉物件之前呼叫 [**保存**](summaryinfo-persist.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5c8bd-109">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="5c8bd-110">若無法這樣做，將會失去現有的資料流程資訊。</span><span class="sxs-lookup"><span data-stu-id="5c8bd-110">Failing to do this loses the existing stream information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8bd-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c8bd-111">Requirements</span></span>



| <span data-ttu-id="5c8bd-112">需求</span><span class="sxs-lookup"><span data-stu-id="5c8bd-112">Requirement</span></span> | <span data-ttu-id="5c8bd-113">值</span><span class="sxs-lookup"><span data-stu-id="5c8bd-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8bd-114">版本</span><span class="sxs-lookup"><span data-stu-id="5c8bd-114">Version</span></span><br/> | <span data-ttu-id="5c8bd-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5c8bd-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5c8bd-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5c8bd-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5c8bd-117">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5c8bd-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5c8bd-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5c8bd-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c8bd-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c8bd-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5c8bd-120">IID</span><span class="sxs-lookup"><span data-stu-id="5c8bd-120">IID</span></span><br/>     | <span data-ttu-id="5c8bd-121">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5c8bd-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




