---
description: 當檔案管理員需要功能表或工具列命令專案的說明字串時，傳送至檔案管理員延伸模組 DLL 程式。
title: 'FMEVENT_HELPSTRING 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841279"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="eba73-103">FMEVENT \_ HELPSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="eba73-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="eba73-104">當檔案管理員需要功能表或工具列命令專案的說明字串時，傳送至檔案管理員延伸模組 DLL 程式。</span><span class="sxs-lookup"><span data-stu-id="eba73-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="eba73-105">參數</span><span class="sxs-lookup"><span data-stu-id="eba73-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba73-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eba73-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eba73-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="eba73-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eba73-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="eba73-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="eba73-109">[**FMS \_ HELPSTRING**](fms-helpstring.md)結構的位址，此結構會傳達命令專案說明字串資料。</span><span class="sxs-lookup"><span data-stu-id="eba73-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="eba73-110">**FMS \_ HELPSTRING** 結構會識別需要說明字串的命令專案，以及其功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eba73-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="eba73-111">然後，應用程式會將適當的說明字串寫入 **FMS \_ HELPSTRING** 結構的 **szHelp** 成員。</span><span class="sxs-lookup"><span data-stu-id="eba73-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eba73-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eba73-112">Return value</span></span>

<span data-ttu-id="eba73-113">如果延伸 DLL 程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="eba73-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eba73-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="eba73-114">Requirements</span></span>



| <span data-ttu-id="eba73-115">需求</span><span class="sxs-lookup"><span data-stu-id="eba73-115">Requirement</span></span> | <span data-ttu-id="eba73-116">值</span><span class="sxs-lookup"><span data-stu-id="eba73-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eba73-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eba73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eba73-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eba73-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="eba73-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eba73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eba73-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eba73-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eba73-121">標頭</span><span class="sxs-lookup"><span data-stu-id="eba73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eba73-122"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="eba73-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eba73-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eba73-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba73-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="eba73-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="eba73-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="eba73-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




