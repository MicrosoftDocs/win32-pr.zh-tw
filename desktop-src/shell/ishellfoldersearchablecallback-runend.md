---
description: 表示搜尋已完成。
title: IShellFolderSearchableCallback：： RunEnd 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: c23d461fdbd175a80a8fa94fcc238f6cf2f89869
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842819"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="fe263-103">IShellFolderSearchableCallback：： RunEnd 方法</span><span class="sxs-lookup"><span data-stu-id="fe263-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="fe263-104">表示搜尋已完成。</span><span class="sxs-lookup"><span data-stu-id="fe263-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe263-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe263-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="fe263-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe263-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe263-107">*>dwreserved* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe263-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe263-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="fe263-108">Type: **DWORD**</span></span>

<span data-ttu-id="fe263-109">保留的。</span><span class="sxs-lookup"><span data-stu-id="fe263-109">Reserved.</span></span> <span data-ttu-id="fe263-110">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="fe263-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe263-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe263-111">Return value</span></span>

<span data-ttu-id="fe263-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fe263-112">Type: **HRESULT**</span></span>

<span data-ttu-id="fe263-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fe263-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe263-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe263-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe263-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe263-115">Requirements</span></span>



| <span data-ttu-id="fe263-116">需求</span><span class="sxs-lookup"><span data-stu-id="fe263-116">Requirement</span></span> | <span data-ttu-id="fe263-117">值</span><span class="sxs-lookup"><span data-stu-id="fe263-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe263-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe263-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe263-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe263-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fe263-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe263-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe263-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe263-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fe263-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fe263-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe263-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe263-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




