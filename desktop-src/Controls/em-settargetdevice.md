---
title: 'EM_SETTARGETDEVICE 訊息 (Richedit .h) '
description: 設定用於 \ 0034 的目標裝置和行寬度; 您所看到的內容是您所得到的 \ 0034; (WYSIWYG) 在 rich edit 控制項中格式化。
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104214"
---
# <a name="em_settargetdevice-message"></a><span data-ttu-id="51272-104">EM \_ SETTARGETDEVICE 訊息</span><span class="sxs-lookup"><span data-stu-id="51272-104">EM\_SETTARGETDEVICE message</span></span>

<span data-ttu-id="51272-105">設定在 rich edit 控制項中，用於「您看到的內容」 (WYSIWYG) 格式的目標裝置和線條寬度。</span><span class="sxs-lookup"><span data-stu-id="51272-105">Sets the target device and line width used for "what you see is what you get" (WYSIWYG) formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="51272-106">參數</span><span class="sxs-lookup"><span data-stu-id="51272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51272-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51272-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51272-108">目標裝置的 HDC。</span><span class="sxs-lookup"><span data-stu-id="51272-108">HDC for the target device.</span></span>

</dd> <dt>

<span data-ttu-id="51272-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51272-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51272-110">用於格式化的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="51272-110">Line width to use for formatting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51272-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="51272-111">Return value</span></span>

<span data-ttu-id="51272-112">如果作業失敗，則傳回值為零，如果成功，則為非零。</span><span class="sxs-lookup"><span data-stu-id="51272-112">The return value is zero if the operation fails, or nonzero if it succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="51272-113">備註</span><span class="sxs-lookup"><span data-stu-id="51272-113">Remarks</span></span>

<span data-ttu-id="51272-114">預設印表機的 HDC 可以依照下列方式取得。</span><span class="sxs-lookup"><span data-stu-id="51272-114">The HDC for the default printer can be obtained as follows.</span></span>


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



<span data-ttu-id="51272-115">如果 *lParam* 為零，則不會建立任何分行符號。</span><span class="sxs-lookup"><span data-stu-id="51272-115">If *lParam* is zero, no line breaks are created.</span></span>

## <a name="requirements"></a><span data-ttu-id="51272-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="51272-116">Requirements</span></span>



| <span data-ttu-id="51272-117">需求</span><span class="sxs-lookup"><span data-stu-id="51272-117">Requirement</span></span> | <span data-ttu-id="51272-118">值</span><span class="sxs-lookup"><span data-stu-id="51272-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51272-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51272-119">Minimum supported client</span></span><br/> | <span data-ttu-id="51272-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51272-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51272-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51272-121">Minimum supported server</span></span><br/> | <span data-ttu-id="51272-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51272-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51272-123">標頭</span><span class="sxs-lookup"><span data-stu-id="51272-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="51272-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="51272-124"><dt>Richedit.h</dt></span></span> </dl> |



 

 





