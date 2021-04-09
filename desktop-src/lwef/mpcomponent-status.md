---
title: 'MPCOMPONENT_STATUS 結構 (MpClient .h) '
description: 元件狀態資訊。
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS 結構舊版 Windows 環境功能
- PMPCOMPONENT_STATUS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685788"
---
# <a name="mpcomponent_status-structure"></a><span data-ttu-id="0f642-105">MPCOMPONENT \_ 狀態結構</span><span class="sxs-lookup"><span data-stu-id="0f642-105">MPCOMPONENT\_STATUS structure</span></span>

<span data-ttu-id="0f642-106">元件狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0f642-106">Component status information.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f642-107">語法</span><span class="sxs-lookup"><span data-stu-id="0f642-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="0f642-108">成員</span><span class="sxs-lookup"><span data-stu-id="0f642-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f642-109">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="0f642-109">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="0f642-110">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="0f642-110">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="0f642-111">元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="0f642-111">Status for the component.</span></span>

</dd> <dt>

<span data-ttu-id="0f642-112">**hResult**</span><span class="sxs-lookup"><span data-stu-id="0f642-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="0f642-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0f642-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="0f642-114">與狀態相關聯的成功或失敗代碼。</span><span class="sxs-lookup"><span data-stu-id="0f642-114">Success or failure code associated with the status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f642-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f642-115">Requirements</span></span>



| <span data-ttu-id="0f642-116">需求</span><span class="sxs-lookup"><span data-stu-id="0f642-116">Requirement</span></span> | <span data-ttu-id="0f642-117">值</span><span class="sxs-lookup"><span data-stu-id="0f642-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f642-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f642-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0f642-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f642-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0f642-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f642-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0f642-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f642-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f642-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0f642-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f642-123"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f642-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





