---
description: 傳回這個列舉值所儲存的元素數目。
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'IEnumWiaItem2：： GetCount 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026327"
---
# <a name="ienumwiaitem2getcount-method"></a><span data-ttu-id="6f538-103">IEnumWiaItem2：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="6f538-103">IEnumWiaItem2::GetCount method</span></span>

<span data-ttu-id="6f538-104">傳回這個列舉值所儲存的元素數目。</span><span class="sxs-lookup"><span data-stu-id="6f538-104">Returns the number of elements stored by this enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f538-105">語法</span><span class="sxs-lookup"><span data-stu-id="6f538-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a><span data-ttu-id="6f538-106">參數</span><span class="sxs-lookup"><span data-stu-id="6f538-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f538-107">*cElt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6f538-107">*cElt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f538-108">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="6f538-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="6f538-109">收到 _ *ULONG*\* 的指標，此專案會接收列舉中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="6f538-109">Receives a pointer to a _ *ULONG*\* that receives the number of elements in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f538-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f538-110">Return value</span></span>

<span data-ttu-id="6f538-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f538-111">Type: **HRESULT**</span></span>

<span data-ttu-id="6f538-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6f538-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f538-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6f538-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f538-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f538-114">Requirements</span></span>



| <span data-ttu-id="6f538-115">需求</span><span class="sxs-lookup"><span data-stu-id="6f538-115">Requirement</span></span> | <span data-ttu-id="6f538-116">值</span><span class="sxs-lookup"><span data-stu-id="6f538-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f538-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f538-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6f538-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f538-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6f538-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f538-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6f538-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f538-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6f538-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6f538-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f538-122"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="6f538-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f538-123">Idl</span><span class="sxs-lookup"><span data-stu-id="6f538-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f538-124"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f538-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




