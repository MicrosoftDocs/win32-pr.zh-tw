---
description: 將列舉參考重設為第一個 IWiaItem2 物件。
ms.assetid: 392e3471-f7fc-456f-a1cc-ab4eb6d3fe18
title: 'IEnumWiaItem2：： Reset 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Reset
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ab4d5a9effbcb003265da53ddc753f63630df51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191578"
---
# <a name="ienumwiaitem2reset-method"></a><span data-ttu-id="b0050-103">IEnumWiaItem2：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="b0050-103">IEnumWiaItem2::Reset method</span></span>

<span data-ttu-id="b0050-104">將列舉參考重設為第一個 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b0050-104">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0050-105">語法</span><span class="sxs-lookup"><span data-stu-id="b0050-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="b0050-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0050-106">Parameters</span></span>

<span data-ttu-id="b0050-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b0050-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0050-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0050-108">Return value</span></span>

<span data-ttu-id="b0050-109">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b0050-109">Type: **HRESULT**</span></span>

<span data-ttu-id="b0050-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b0050-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0050-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b0050-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0050-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0050-112">Requirements</span></span>



| <span data-ttu-id="b0050-113">需求</span><span class="sxs-lookup"><span data-stu-id="b0050-113">Requirement</span></span> | <span data-ttu-id="b0050-114">值</span><span class="sxs-lookup"><span data-stu-id="b0050-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0050-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0050-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b0050-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0050-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b0050-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0050-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b0050-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0050-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b0050-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b0050-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0050-120"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="b0050-120"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0050-121">Idl</span><span class="sxs-lookup"><span data-stu-id="b0050-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0050-122"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0050-122"><dt>Wia.idl</dt></span></span> </dl> |



 

 




