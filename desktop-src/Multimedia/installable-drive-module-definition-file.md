---
title: 可安裝的磁片磁碟機 Module-Definition 檔案
description: 可安裝的磁片磁碟機 Module-Definition 檔案
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- 可安裝的驅動程式、模組定義檔
- 可安裝的驅動程式、DEF 檔案
- nstallable 驅動程式，DriverProc 函式
- DriverProc 函式
- 模組定義檔
- DEF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023365"
---
# <a name="installable-drive-module-definition-file"></a><span data-ttu-id="9742e-109">可安裝的磁片磁碟機 Module-Definition 檔案</span><span class="sxs-lookup"><span data-stu-id="9742e-109">Installable Drive Module-Definition File</span></span>

<span data-ttu-id="9742e-110">模組定義 (。DEF) 可安裝驅動程式的檔案會將驅動程式命名為驅動程式、匯出 [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) 函式，並定義驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="9742e-110">The module-definition (.DEF) file of an installable driver names the driver, exports the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function, and defines a driver description.</span></span> <span data-ttu-id="9742e-111">下列範例顯示可安裝驅動程式的典型模組定義檔：</span><span class="sxs-lookup"><span data-stu-id="9742e-111">The following example shows a typical module-definition file for an installable driver:</span></span>


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



<span data-ttu-id="9742e-112">某些安裝應用程式可能會開啟驅動程式，並取得安裝驅動程式時所要使用的描述行。</span><span class="sxs-lookup"><span data-stu-id="9742e-112">Some installation applications may open the driver and retrieve the description line to use when installing the driver.</span></span> <span data-ttu-id="9742e-113">為了與這些安裝應用程式保持相容，描述行的格式應該如下：</span><span class="sxs-lookup"><span data-stu-id="9742e-113">To remain compatible with these installation applications, the description line should have this form:</span></span>

<span data-ttu-id="9742e-114">**DESCRIPTION**  *alias* \[ ，*alias* \] ... **:* \* \* text*</span><span class="sxs-lookup"><span data-stu-id="9742e-114">**DESCRIPTION**  *alias*\[,*alias*\]...\**:\*\*\*text*</span></span>

<span data-ttu-id="9742e-115">*別名* 會指定應用程式可用來開啟驅動程式之驅動程式的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="9742e-115">The *alias* specifies a unique name for the driver that applications can use to open the driver.</span></span> <span data-ttu-id="9742e-116">別名也可作為與登錄中驅動程式相關聯的值名稱。</span><span class="sxs-lookup"><span data-stu-id="9742e-116">The alias also serves as the value name associated with the driver in the registry.</span></span> <span data-ttu-id="9742e-117">多個別名會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="9742e-117">Multiple aliases are separated by commas.</span></span> <span data-ttu-id="9742e-118">此 *文字* 描述驅動程式的用途。</span><span class="sxs-lookup"><span data-stu-id="9742e-118">The *text* describes the purpose of the driver.</span></span>

 

 