---
description: 從登錄將字串清單載入最近使用的 (MRU) 清單中。
title: IACLCustomMRU：： Initialize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841229"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="42145-103">IACLCustomMRU：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="42145-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="42145-104">從登錄將字串清單載入最近使用的 (MRU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="42145-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="42145-105">語法</span><span class="sxs-lookup"><span data-stu-id="42145-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="42145-106">參數</span><span class="sxs-lookup"><span data-stu-id="42145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42145-107">*pwszMRURegKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42145-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42145-108">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="42145-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="42145-109">緩衝區的指標，其中包含保存 MRU 清單字串的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="42145-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="42145-110">*dwMax* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42145-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42145-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="42145-111">Type: **DWORD**</span></span>

<span data-ttu-id="42145-112">可從 *pwszMRURegKey* 取得的最大專案數。</span><span class="sxs-lookup"><span data-stu-id="42145-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42145-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="42145-113">Return value</span></span>

<span data-ttu-id="42145-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="42145-114">Type: **HRESULT**</span></span>

<span data-ttu-id="42145-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="42145-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42145-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="42145-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="42145-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="42145-117">Requirements</span></span>



| <span data-ttu-id="42145-118">需求</span><span class="sxs-lookup"><span data-stu-id="42145-118">Requirement</span></span> | <span data-ttu-id="42145-119">值</span><span class="sxs-lookup"><span data-stu-id="42145-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42145-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42145-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42145-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42145-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="42145-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42145-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42145-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42145-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




