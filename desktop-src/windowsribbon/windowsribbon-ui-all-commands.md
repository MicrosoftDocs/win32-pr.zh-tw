---
title: 'UI_ALL_COMMANDS (Uiribbon) '
description: 指定常數，識別標記資源檔中所宣告的命令集合。
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966498"
---
# <a name="ui_all_commands"></a><span data-ttu-id="b7e5d-103">UI \_ 所有 \_ 命令</span><span class="sxs-lookup"><span data-stu-id="b7e5d-103">UI\_ALL\_COMMANDS</span></span>

<span data-ttu-id="b7e5d-104">指定常數，識別標記資源檔中所宣告的命令集合。</span><span class="sxs-lookup"><span data-stu-id="b7e5d-104">Specifies a constant that identifies the collection of Commands declared in the Markup resource file.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e5d-105">備註</span><span class="sxs-lookup"><span data-stu-id="b7e5d-105">Remarks</span></span>

<span data-ttu-id="b7e5d-106">**UI \_當 \_** 需要在所有命令中存取類似的屬性時，所有命令都很有用。</span><span class="sxs-lookup"><span data-stu-id="b7e5d-106">**UI\_ALL\_COMMANDS** is useful when it is necessary to access similar properties across all Commands.</span></span> <span data-ttu-id="b7e5d-107">例如，您可以透過查詢主機應用程式的新屬性值，將 **\_ 所有 \_ 命令** 都傳遞給 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ，以使所有功能區命令失效並重新整理。</span><span class="sxs-lookup"><span data-stu-id="b7e5d-107">For example, **UI\_ALL\_COMMANDS** can be passed to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) to invalidate and refresh all Ribbon Commands by querying the host application for new property values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e5d-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7e5d-108">Requirements</span></span>



| <span data-ttu-id="b7e5d-109">需求</span><span class="sxs-lookup"><span data-stu-id="b7e5d-109">Requirement</span></span> | <span data-ttu-id="b7e5d-110">值</span><span class="sxs-lookup"><span data-stu-id="b7e5d-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e5d-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7e5d-111">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e5d-112">Windows 7、windows Vista （含 SP2）和平臺更新（僅適用于 Windows Vista \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="b7e5d-112">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b7e5d-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7e5d-113">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e5d-114">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新（僅適用于 Windows Server 2008 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="b7e5d-114">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b7e5d-115">標頭</span><span class="sxs-lookup"><span data-stu-id="b7e5d-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e5d-116"><dt>Uiribbon。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e5d-116"><dt>Uiribbon.h</dt></span></span> </dl>                                             |
| <span data-ttu-id="b7e5d-117">Idl</span><span class="sxs-lookup"><span data-stu-id="b7e5d-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7e5d-118"><dt>Uiribbon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7e5d-118"><dt>Uiribbon.idl</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="b7e5d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7e5d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e5d-120">常數和列舉</span><span class="sxs-lookup"><span data-stu-id="b7e5d-120">Constants and Enumerations</span></span>](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

