---
description: 操縱文字會議描述。
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: 'ITConferenceBlob 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995749"
---
# <a name="itconferenceblob-interface"></a><span data-ttu-id="d731d-103">ITConferenceBlob 介面</span><span class="sxs-lookup"><span data-stu-id="d731d-103">ITConferenceBlob interface</span></span>

<span data-ttu-id="d731d-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="d731d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d731d-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d731d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d731d-106">**ITConferenceBlob** 介面會操控文字會議描述。</span><span class="sxs-lookup"><span data-stu-id="d731d-106">The **ITConferenceBlob** interface manipulates a textual conference description.</span></span> <span data-ttu-id="d731d-107">介面的設計目的是要與會議描述的格式和語法無關。</span><span class="sxs-lookup"><span data-stu-id="d731d-107">The interface is intended to be independent of the format and syntax of the conference description.</span></span> <span data-ttu-id="d731d-108">若要操作會議描述的特定層面，應用程式必須查詢另一個介面。</span><span class="sxs-lookup"><span data-stu-id="d731d-108">To manipulate specific aspects of the conference description, the application must query for another interface.</span></span> <span data-ttu-id="d731d-109">目前只支援 SDP 會議說明;應用程式必須使用 **QueryInterface** 進行 [**ITSdp**](itsdp.md) ，才能存取 SDP 會議描述的各種欄位。</span><span class="sxs-lookup"><span data-stu-id="d731d-109">Currently, only SDP conference descriptions are supported; the application must use **QueryInterface** for [**ITSdp**](itsdp.md) to access the various fields of the SDP conference description.</span></span> <span data-ttu-id="d731d-110">**ITConferenceBlob** 介面是藉由在 [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)上呼叫 **QueryInterface** 來建立。</span><span class="sxs-lookup"><span data-stu-id="d731d-110">The **ITConferenceBlob** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="d731d-111">成員</span><span class="sxs-lookup"><span data-stu-id="d731d-111">Members</span></span>

<span data-ttu-id="d731d-112">**ITConferenceBlob** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="d731d-112">The **ITConferenceBlob** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d731d-113">**ITConferenceBlob** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d731d-113">**ITConferenceBlob** also has these types of members:</span></span>

-   [<span data-ttu-id="d731d-114">方法</span><span class="sxs-lookup"><span data-stu-id="d731d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d731d-115">方法</span><span class="sxs-lookup"><span data-stu-id="d731d-115">Methods</span></span>

<span data-ttu-id="d731d-116">**ITConferenceBlob** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d731d-116">The **ITConferenceBlob** interface has these methods.</span></span>



| <span data-ttu-id="d731d-117">方法</span><span class="sxs-lookup"><span data-stu-id="d731d-117">Method</span></span>                                                             | <span data-ttu-id="d731d-118">描述</span><span class="sxs-lookup"><span data-stu-id="d731d-118">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d731d-119">**取得 \_ CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="d731d-119">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)     | <span data-ttu-id="d731d-120">取得 blob [**\_ 字元集 \_**](blob-character-set.md) 指標，其中 BLOB 字元是否為 ASCII、Unicode 等等。</span><span class="sxs-lookup"><span data-stu-id="d731d-120">Gets the [**BLOB\_CHARACTER\_SET**](blob-character-set.md) indicator of whether blob characters are in ASCII, Unicode, and so on.</span></span><br/> |
| [<span data-ttu-id="d731d-121">**取得 \_ ConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="d731d-121">**get\_ConferenceBlob**</span></span>](itconferenceblob-get-conferenceblob.md) | <span data-ttu-id="d731d-122">取得會議 blob 的指標。</span><span class="sxs-lookup"><span data-stu-id="d731d-122">Gets a pointer to the conference blob.</span></span><br/>                                                                                             |
| [<span data-ttu-id="d731d-123">**Init**</span><span class="sxs-lookup"><span data-stu-id="d731d-123">**Init**</span></span>](itconferenceblob-init.md)                              | <span data-ttu-id="d731d-124">初始化會議 blob。</span><span class="sxs-lookup"><span data-stu-id="d731d-124">Initializes the conference blob.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d731d-125">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="d731d-125">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)    | <span data-ttu-id="d731d-126">認可會議 blob 的變更。</span><span class="sxs-lookup"><span data-stu-id="d731d-126">Commits changes to the conference blob.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="d731d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d731d-127">Requirements</span></span>



| <span data-ttu-id="d731d-128">需求</span><span class="sxs-lookup"><span data-stu-id="d731d-128">Requirement</span></span> | <span data-ttu-id="d731d-129">值</span><span class="sxs-lookup"><span data-stu-id="d731d-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d731d-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d731d-130">TAPI version</span></span><br/> | <span data-ttu-id="d731d-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d731d-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d731d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="d731d-132">Header</span></span><br/>       | <dl> <span data-ttu-id="d731d-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d731d-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d731d-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="d731d-134">Library</span></span><br/>      | <dl> <span data-ttu-id="d731d-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="d731d-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d731d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d731d-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="d731d-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d731d-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

