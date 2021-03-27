---
description: 通知 appbar 工作列的自動隱藏或 alwayson 狀態已變更&\# 郵件; 也就是使用者已選取或清除 &\# 0034;一律在頂端&\# 0034; 或 &\# 0034;自動隱藏&\# 0034; 工具列的屬性工作表上的核取方塊。
title: 'ABN_STATECHANGE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847799"
---
# <a name="abn_statechange-message"></a><span data-ttu-id="289bb-103">ABN \_ STATECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="289bb-103">ABN\_STATECHANGE message</span></span>

<span data-ttu-id="289bb-104">通知 appbar 工作列的自動隱藏或 alwayson 狀態已變更，也就是使用者已選取或清除工作列屬性工作表上的 [永遠開啟] 或 [自動隱藏] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="289bb-104">Notifies an appbar that the taskbar's autohide or always-on-top state has changed that is, the user has selected or cleared the "Always on top" or "Auto hide" check box on the taskbar's property sheet.</span></span>


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a><span data-ttu-id="289bb-105">參數</span><span class="sxs-lookup"><span data-stu-id="289bb-105">Parameters</span></span>

<span data-ttu-id="289bb-106">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="289bb-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="289bb-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="289bb-107">Return value</span></span>

<span data-ttu-id="289bb-108">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="289bb-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="289bb-109">備註</span><span class="sxs-lookup"><span data-stu-id="289bb-109">Remarks</span></span>

<span data-ttu-id="289bb-110">Appbar 可以使用此通知訊息，將其狀態設定為符合工作列的狀態（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="289bb-110">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="289bb-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="289bb-111">Requirements</span></span>



| <span data-ttu-id="289bb-112">需求</span><span class="sxs-lookup"><span data-stu-id="289bb-112">Requirement</span></span> | <span data-ttu-id="289bb-113">值</span><span class="sxs-lookup"><span data-stu-id="289bb-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="289bb-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="289bb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="289bb-115">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="289bb-115">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="289bb-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="289bb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="289bb-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="289bb-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="289bb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="289bb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="289bb-119"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="289bb-119"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




