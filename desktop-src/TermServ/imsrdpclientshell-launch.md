---
title: IMsRdpClientShell 啟動方法
description: 從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端檔案內容。
ms.assetid: a0aa12e4-8b6f-4a3a-a6b8-f5def0b8bd90
ms.tgt_platform: multiple
keywords:
- 啟動方法遠端桌面服務
- 啟動方法遠端桌面服務，IMsRdpClientShell 介面
- IMsRdpClientShell 介面遠端桌面服務，啟動方法
topic_type:
- apiref
api_name:
- IMsRdpClientShell.Launch
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae895d8a12824c6aca1dcbd69c5055b3ca6f3e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384177"
---
# <a name="imsrdpclientshelllaunch-method"></a><span data-ttu-id="0fbb2-106">IMsRdpClientShell：：啟動方法</span><span class="sxs-lookup"><span data-stu-id="0fbb2-106">IMsRdpClientShell::Launch method</span></span>

<span data-ttu-id="0fbb2-107">從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端檔案內容。</span><span class="sxs-lookup"><span data-stu-id="0fbb2-107">Launches remote file content from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbb2-108">語法</span><span class="sxs-lookup"><span data-stu-id="0fbb2-108">Syntax</span></span>


```C++
HRESULT Launch();
```



## <a name="parameters"></a><span data-ttu-id="0fbb2-109">參數</span><span class="sxs-lookup"><span data-stu-id="0fbb2-109">Parameters</span></span>

<span data-ttu-id="0fbb2-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0fbb2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fbb2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fbb2-111">Return value</span></span>

<span data-ttu-id="0fbb2-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0fbb2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0fbb2-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0fbb2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fbb2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fbb2-114">Requirements</span></span>



| <span data-ttu-id="0fbb2-115">需求</span><span class="sxs-lookup"><span data-stu-id="0fbb2-115">Requirement</span></span> | <span data-ttu-id="0fbb2-116">值</span><span class="sxs-lookup"><span data-stu-id="0fbb2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbb2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fbb2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0fbb2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fbb2-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0fbb2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fbb2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0fbb2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fbb2-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0fbb2-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0fbb2-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="0fbb2-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fbb2-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0fbb2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0fbb2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fbb2-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fbb2-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0fbb2-125">IID</span><span class="sxs-lookup"><span data-stu-id="0fbb2-125">IID</span></span><br/>                      | <span data-ttu-id="0fbb2-126">IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="0fbb2-126">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="0fbb2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fbb2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fbb2-128">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="0fbb2-128">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





