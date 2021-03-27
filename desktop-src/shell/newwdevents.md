---
description: 藉由啟用在 wizard 中裝載的伺服器端頁面，來擴充 WebWizardHost 物件，以確認使用者已通過 Microsoft 帳戶驗證。
ms.assetid: 44f2431c-82a2-4142-bf20-55fdd0c88008
title: 'NewWDEvents 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d1387724609ab29852f1b6a2a8f9df5032def1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848297"
---
# <a name="newwdevents-object"></a><span data-ttu-id="b4253-103">NewWDEvents 物件</span><span class="sxs-lookup"><span data-stu-id="b4253-103">NewWDEvents object</span></span>

<span data-ttu-id="b4253-104">藉由啟用在 wizard 中裝載的伺服器端頁面，來擴充 [**WebWizardHost**](webwizardhost.md) 物件，以確認使用者已通過 Microsoft 帳戶驗證。</span><span class="sxs-lookup"><span data-stu-id="b4253-104">Extends the [**WebWizardHost**](webwizardhost.md) object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="members"></a><span data-ttu-id="b4253-105">成員</span><span class="sxs-lookup"><span data-stu-id="b4253-105">Members</span></span>

<span data-ttu-id="b4253-106">**NewWDEvents** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b4253-106">The **NewWDEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="b4253-107">方法</span><span class="sxs-lookup"><span data-stu-id="b4253-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b4253-108">方法</span><span class="sxs-lookup"><span data-stu-id="b4253-108">Methods</span></span>

<span data-ttu-id="b4253-109">**NewWDEvents** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b4253-109">The **NewWDEvents** object has these methods.</span></span>



| <span data-ttu-id="b4253-110">方法</span><span class="sxs-lookup"><span data-stu-id="b4253-110">Method</span></span>                                                            | <span data-ttu-id="b4253-111">描述</span><span class="sxs-lookup"><span data-stu-id="b4253-111">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4253-112">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="b4253-112">**PassportAuthenticate**</span></span>](inewwdevents-passportauthenticate.md) | <span data-ttu-id="b4253-113">在嚮導中啟用裝載的伺服器端頁面，以確認使用者已通過 Microsoft 帳戶驗證。</span><span class="sxs-lookup"><span data-stu-id="b4253-113">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b4253-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4253-114">Requirements</span></span>



| <span data-ttu-id="b4253-115">需求</span><span class="sxs-lookup"><span data-stu-id="b4253-115">Requirement</span></span> | <span data-ttu-id="b4253-116">值</span><span class="sxs-lookup"><span data-stu-id="b4253-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4253-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4253-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b4253-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4253-118">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="b4253-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4253-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b4253-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4253-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b4253-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b4253-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4253-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4253-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b4253-123">Idl</span><span class="sxs-lookup"><span data-stu-id="b4253-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4253-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4253-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b4253-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b4253-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4253-126"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b4253-126"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




