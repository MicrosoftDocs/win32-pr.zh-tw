---
description: SummaryInfo 物件的保存方法會格式化，並將先前儲存的屬性寫入標準 SummaryInformation 資料流程。
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. 保存方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993386"
---
# <a name="summaryinfopersist-method"></a><span data-ttu-id="05b32-103">SummaryInfo. 保存方法</span><span class="sxs-lookup"><span data-stu-id="05b32-103">SummaryInfo.Persist method</span></span>

<span data-ttu-id="05b32-104">[**SummaryInfo**](summaryinfo-object.md)物件的 **保存** 方法會格式化，並將先前儲存的屬性寫入標準 SummaryInformation 資料流程。</span><span class="sxs-lookup"><span data-stu-id="05b32-104">The **Persist** method of the [**SummaryInfo**](summaryinfo-object.md) object formats and writes the previously stored properties into the standard SummaryInformation stream.</span></span> <span data-ttu-id="05b32-105">如果無法成功寫入資料流程，它就會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="05b32-105">It generates an error if the stream cannot be successfully written.</span></span> <span data-ttu-id="05b32-106">只有在設定所有屬性值之後，才會呼叫這個方法一次。</span><span class="sxs-lookup"><span data-stu-id="05b32-106">This method may only be called once after all the property values have been set.</span></span> <span data-ttu-id="05b32-107">寫入資料流程之後，仍然可以讀取屬性。</span><span class="sxs-lookup"><span data-stu-id="05b32-107">Properties may still be read after the stream is written.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b32-108">語法</span><span class="sxs-lookup"><span data-stu-id="05b32-108">Syntax</span></span>


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a><span data-ttu-id="05b32-109">參數</span><span class="sxs-lookup"><span data-stu-id="05b32-109">Parameters</span></span>

<span data-ttu-id="05b32-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="05b32-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05b32-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="05b32-111">Return value</span></span>

<span data-ttu-id="05b32-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="05b32-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="05b32-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="05b32-113">Requirements</span></span>



| <span data-ttu-id="05b32-114">需求</span><span class="sxs-lookup"><span data-stu-id="05b32-114">Requirement</span></span> | <span data-ttu-id="05b32-115">值</span><span class="sxs-lookup"><span data-stu-id="05b32-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05b32-116">版本</span><span class="sxs-lookup"><span data-stu-id="05b32-116">Version</span></span><br/> | <span data-ttu-id="05b32-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="05b32-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05b32-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="05b32-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05b32-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="05b32-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="05b32-120">DLL</span><span class="sxs-lookup"><span data-stu-id="05b32-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="05b32-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05b32-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="05b32-122">IID</span><span class="sxs-lookup"><span data-stu-id="05b32-122">IID</span></span><br/>     | <span data-ttu-id="05b32-123">IID \_ ISummaryInfo 定義為 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="05b32-123">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



 

 




