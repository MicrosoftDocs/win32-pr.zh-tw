---
title: 'EM_EXSETSEL 訊息 (Richedit .h) '
description: 在 Microsoft Rich Edit 控制項中，選取 (COM) 物件的字元或元件物件模型範圍。
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843820"
---
# <a name="em_exsetsel-message"></a><span data-ttu-id="c7018-104">EM \_ EXSETSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="c7018-104">EM\_EXSETSEL message</span></span>

<span data-ttu-id="c7018-105">在 Microsoft Rich Edit 控制項中，選取 (COM) 物件的字元或元件物件模型範圍。</span><span class="sxs-lookup"><span data-stu-id="c7018-105">Selects a range of characters or Component Object Model (COM) objects in a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7018-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7018-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7018-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7018-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="c7018-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c7018-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7018-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7018-110">指定選取範圍的 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) 結構。</span><span class="sxs-lookup"><span data-stu-id="c7018-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that specifies the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7018-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7018-111">Return value</span></span>

<span data-ttu-id="c7018-112">傳回值是實際設定的選取專案。</span><span class="sxs-lookup"><span data-stu-id="c7018-112">The return value is the selection that is actually set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7018-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7018-113">Requirements</span></span>



| <span data-ttu-id="c7018-114">需求</span><span class="sxs-lookup"><span data-stu-id="c7018-114">Requirement</span></span> | <span data-ttu-id="c7018-115">值</span><span class="sxs-lookup"><span data-stu-id="c7018-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7018-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7018-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c7018-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7018-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7018-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7018-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c7018-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7018-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7018-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c7018-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7018-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7018-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





