---
description: Windows 映像取得 (WIA) Api 會以 HRESULT 傳回值傳回其完成狀態。
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: WIA 錯誤資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971007"
---
# <a name="wia-error-information"></a><span data-ttu-id="93f0a-103">WIA 錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="93f0a-103">WIA Error Information</span></span>

<span data-ttu-id="93f0a-104">Windows 映像取得 (WIA) Api 會以 HRESULT 傳回值傳回其完成狀態。</span><span class="sxs-lookup"><span data-stu-id="93f0a-104">The Windows Image Acquisition (WIA)APIs return their completion status in an HRESULT return value.</span></span> <span data-ttu-id="93f0a-105">應用程式會根據設備 WIA 常數來檢查這些傳回值 \_ ，以判斷錯誤是否需要使用者介入來清除（例如卡紙路徑），並將它們回報給使用者。</span><span class="sxs-lookup"><span data-stu-id="93f0a-105">Applications check these return values against the FACILITY\_WIA constant to determine whether the error requires user intervention to clear, such as a jammed paper path, and report them to the user.</span></span> <span data-ttu-id="93f0a-106">此外，所有驅動層級錯誤都會詳細記錄到事件記錄檔，並使用裝置迷你驅動程式提供的錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="93f0a-106">In addition, all driver-level errors are logged in detail to the event log, using error strings provided by the device minidriver.</span></span> <span data-ttu-id="93f0a-107">如需 WIA 特定錯誤碼的清單，請參閱 [錯誤碼](-wia-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="93f0a-107">For a listing of WIA-specific error codes, see [Error Codes](-wia-error-codes.md).</span></span>

 

 



