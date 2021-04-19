---
description: ITQOSApplicationID 介面會公開方法，讓應用程式取得目前呼叫的 QOS 識別碼。
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: 'ITQOSApplicationID 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993680"
---
# <a name="itqosapplicationid-interface"></a><span data-ttu-id="15bf3-103">ITQOSApplicationID 介面</span><span class="sxs-lookup"><span data-stu-id="15bf3-103">ITQOSApplicationID interface</span></span>

<span data-ttu-id="15bf3-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="15bf3-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="15bf3-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="15bf3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="15bf3-106">**ITQOSApplicationID** 介面會公開方法，讓應用程式取得目前呼叫的 QOS 識別碼。</span><span class="sxs-lookup"><span data-stu-id="15bf3-106">The **ITQOSApplicationID** interface exposes a method that allows an application to get the QOS identifier for the current call.</span></span>

<span data-ttu-id="15bf3-107">此介面是由 [IPCONF MSP](ipconf-msp.md) 所執行，而且只會在呼叫使用 IP 會議時公開。</span><span class="sxs-lookup"><span data-stu-id="15bf3-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and is exposed only when a call uses IP Conferencing.</span></span>

## <a name="members"></a><span data-ttu-id="15bf3-108">成員</span><span class="sxs-lookup"><span data-stu-id="15bf3-108">Members</span></span>

<span data-ttu-id="15bf3-109">**ITQOSApplicationID** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="15bf3-109">The **ITQOSApplicationID** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="15bf3-110">**ITQOSApplicationID** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15bf3-110">**ITQOSApplicationID** also has these types of members:</span></span>

-   [<span data-ttu-id="15bf3-111">方法</span><span class="sxs-lookup"><span data-stu-id="15bf3-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15bf3-112">方法</span><span class="sxs-lookup"><span data-stu-id="15bf3-112">Methods</span></span>

<span data-ttu-id="15bf3-113">**ITQOSApplicationID** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="15bf3-113">The **ITQOSApplicationID** interface has these methods.</span></span>



| <span data-ttu-id="15bf3-114">方法</span><span class="sxs-lookup"><span data-stu-id="15bf3-114">Method</span></span>                                                                | <span data-ttu-id="15bf3-115">描述</span><span class="sxs-lookup"><span data-stu-id="15bf3-115">Description</span></span>                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="15bf3-116">**SetQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="15bf3-116">**SetQOSApplicationID**</span></span>](itqosapplicationid-setqosapplicationid.md) | <span data-ttu-id="15bf3-117">設定 QOS 識別碼。</span><span class="sxs-lookup"><span data-stu-id="15bf3-117">Sets the QOS identifier.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="15bf3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="15bf3-118">Requirements</span></span>



| <span data-ttu-id="15bf3-119">需求</span><span class="sxs-lookup"><span data-stu-id="15bf3-119">Requirement</span></span> | <span data-ttu-id="15bf3-120">值</span><span class="sxs-lookup"><span data-stu-id="15bf3-120">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15bf3-121">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="15bf3-121">TAPI version</span></span><br/> | <span data-ttu-id="15bf3-122">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="15bf3-122">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="15bf3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="15bf3-123">Header</span></span><br/>       | <dl> <span data-ttu-id="15bf3-124"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="15bf3-124"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15bf3-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="15bf3-125">Library</span></span><br/>      | <dl> <span data-ttu-id="15bf3-126"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="15bf3-126"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="15bf3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="15bf3-127">DLL</span></span><br/>          | <dl> <span data-ttu-id="15bf3-128"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15bf3-128"><dt>Tapi3.dll</dt></span></span> </dl> |



 

