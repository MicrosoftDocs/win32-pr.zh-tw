---
description: 將專案新增至最近使用的 (MRU) 清單中。
title: IACLCustomMRU：： AddMRUString 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841999"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="d5a40-103">IACLCustomMRU：： AddMRUString 方法</span><span class="sxs-lookup"><span data-stu-id="d5a40-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="d5a40-104">將專案新增至最近使用的 (MRU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="d5a40-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a40-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5a40-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="d5a40-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5a40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a40-107">*pwszEntry* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5a40-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a40-108">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d5a40-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d5a40-109">包含新專案之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d5a40-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a40-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5a40-110">Return value</span></span>

<span data-ttu-id="d5a40-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d5a40-111">Type: **HRESULT**</span></span>

<span data-ttu-id="d5a40-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d5a40-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d5a40-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d5a40-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a40-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5a40-114">Requirements</span></span>



| <span data-ttu-id="d5a40-115">需求</span><span class="sxs-lookup"><span data-stu-id="d5a40-115">Requirement</span></span> | <span data-ttu-id="d5a40-116">值</span><span class="sxs-lookup"><span data-stu-id="d5a40-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5a40-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5a40-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a40-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5a40-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d5a40-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5a40-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a40-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5a40-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




