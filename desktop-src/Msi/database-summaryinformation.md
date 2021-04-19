---
description: 資料庫物件的 SummaryInformation 屬性會傳回 SummaryInfo 物件，此物件可用來檢查、更新和加入屬性至摘要資訊資料流程。
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: SummaryInformation 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000484"
---
# <a name="databasesummaryinformation-property"></a><span data-ttu-id="b547b-103">SummaryInformation 屬性</span><span class="sxs-lookup"><span data-stu-id="b547b-103">Database.SummaryInformation property</span></span>

<span data-ttu-id="b547b-104">[**資料庫**](database-object.md)物件的 **SummaryInformation** 屬性會傳回 [**SummaryInfo**](summaryinfo-object.md)物件，此物件可用來檢查、更新和加入屬性至 [摘要資訊資料流程](summary-information-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="b547b-104">The **SummaryInformation** property of the [**Database**](database-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the [summary information stream](summary-information-stream.md).</span></span>

<span data-ttu-id="b547b-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b547b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b547b-106">語法</span><span class="sxs-lookup"><span data-stu-id="b547b-106">Syntax</span></span>


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="b547b-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="b547b-107">Property value</span></span>

<span data-ttu-id="b547b-108">要加入或修改之屬性的最大數目。</span><span class="sxs-lookup"><span data-stu-id="b547b-108">The maximum number of properties to be added or modified.</span></span> <span data-ttu-id="b547b-109">這個參數是必要參數，可用來在串流產生期間配置足夠的工作記憶體。</span><span class="sxs-lookup"><span data-stu-id="b547b-109">This parameter is required and used to allocate sufficient working memory during the stream generation.</span></span> <span data-ttu-id="b547b-110">不需要儲存此屬性數目。</span><span class="sxs-lookup"><span data-stu-id="b547b-110">It is not required to store this number of properties.</span></span> <span data-ttu-id="b547b-111">如果資料庫是開啟唯讀，以防止更新資料流程，就必須使用零值。</span><span class="sxs-lookup"><span data-stu-id="b547b-111">A value of zero must be used if the database is opened read-only to prevent the stream from being updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="b547b-112">備註</span><span class="sxs-lookup"><span data-stu-id="b547b-112">Remarks</span></span>

<span data-ttu-id="b547b-113">如果使用大於0的 *maxProperties* 值來開啟現有的摘要資訊資料流程，就必須在關閉物件之前呼叫 [**保存**](summaryinfo-persist.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b547b-113">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="b547b-114">若無法這樣做，將會遺失現有的資料流程資訊。</span><span class="sxs-lookup"><span data-stu-id="b547b-114">Failing to do this will lose the existing stream information.</span></span>

<span data-ttu-id="b547b-115">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b547b-115">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b547b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b547b-116">Requirements</span></span>



| <span data-ttu-id="b547b-117">需求</span><span class="sxs-lookup"><span data-stu-id="b547b-117">Requirement</span></span> | <span data-ttu-id="b547b-118">值</span><span class="sxs-lookup"><span data-stu-id="b547b-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b547b-119">版本</span><span class="sxs-lookup"><span data-stu-id="b547b-119">Version</span></span><br/> | <span data-ttu-id="b547b-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="b547b-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b547b-121">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="b547b-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b547b-122">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b547b-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b547b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b547b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b547b-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b547b-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b547b-125">IID</span><span class="sxs-lookup"><span data-stu-id="b547b-125">IID</span></span><br/>     | <span data-ttu-id="b547b-126">IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b547b-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




