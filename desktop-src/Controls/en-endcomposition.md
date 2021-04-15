---
title: 'EN_ENDCOMPOSITION (Richedit 的通知碼) '
description: 通知 rich edit 控制項父視窗，指出使用者已輸入新資料，或在使用 IME 或文字服務架構時完成輸入資料。
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464424"
---
# <a name="en_endcomposition-notification-code"></a><span data-ttu-id="48ac8-104">EN \_ ENDCOMPOSITION 通知碼</span><span class="sxs-lookup"><span data-stu-id="48ac8-104">EN\_ENDCOMPOSITION notification code</span></span>

<span data-ttu-id="48ac8-105">通知 rich edit 控制項父視窗，指出使用者已輸入新資料，或在使用 IME 或 [文字服務架構](/windows/desktop/TSF/text-services-framework)時完成輸入資料。</span><span class="sxs-lookup"><span data-stu-id="48ac8-105">Notifies a rich edit control parent window that the user has entered new data or has finished entering data while using IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a><span data-ttu-id="48ac8-106">參數</span><span class="sxs-lookup"><span data-stu-id="48ac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48ac8-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48ac8-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48ac8-108">[**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify)結構，可接收有關結束組合條件的資訊。</span><span class="sxs-lookup"><span data-stu-id="48ac8-108">A [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) structure that receives information about the end composition condition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48ac8-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="48ac8-109">Requirements</span></span>



| <span data-ttu-id="48ac8-110">需求</span><span class="sxs-lookup"><span data-stu-id="48ac8-110">Requirement</span></span> | <span data-ttu-id="48ac8-111">值</span><span class="sxs-lookup"><span data-stu-id="48ac8-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48ac8-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48ac8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="48ac8-113">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48ac8-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="48ac8-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48ac8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="48ac8-115">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48ac8-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48ac8-116">標頭</span><span class="sxs-lookup"><span data-stu-id="48ac8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="48ac8-117"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="48ac8-117"><dt>Richedit.h</dt></span></span> </dl> |



 

