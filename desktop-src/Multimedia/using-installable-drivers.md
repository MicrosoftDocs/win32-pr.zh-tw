---
title: 使用可安裝的驅動程式
description: 使用可安裝的驅動程式
ms.assetid: 23680369-92f9-4558-aa95-f2f44734cece
keywords:
- Windows 多媒體、可安裝的驅動程式
- 多媒體、可安裝的驅動程式
- 可安裝的驅動程式，關於
- DriverProc 函式
- 可安裝的驅動程式，DriverProc 函式
- 可安裝的驅動程式，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd8573e017eb8bee9b8f1e6054fdd529b724335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314665"
---
# <a name="using-installable-drivers"></a><span data-ttu-id="b6671-109">使用可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="b6671-109">Using Installable Drivers</span></span>

<span data-ttu-id="b6671-110">您可以使用可安裝的驅動程式，為應用程式或 Dll 提供存取裝置或一組實用常式的標準方式。</span><span class="sxs-lookup"><span data-stu-id="b6671-110">You use installable drivers to give applications or DLLs a standard way to access a device or a set of useful routines.</span></span> <span data-ttu-id="b6671-111">下列各節說明如何使用 [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) 函式建立可安裝的驅動程式，以及如何開啟可安裝的驅動程式，並指示它執行有用的工作。</span><span class="sxs-lookup"><span data-stu-id="b6671-111">The following sections show how to create an installable driver by using a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function and how to open an installable driver and direct it to carry out useful tasks.</span></span>

 

 