---
title: 裝置名稱
description: 裝置名稱
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462469"
---
# <a name="device-names"></a><span data-ttu-id="bf347-103">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="bf347-103">Device Names</span></span>

<span data-ttu-id="bf347-104">針對每個裝置類型，可能會有數個 MCI 驅動程式共用命令集，但操作不同的資料格式。</span><span class="sxs-lookup"><span data-stu-id="bf347-104">For each device type, there might be several MCI drivers that share the command set but operate on different data formats.</span></span> <span data-ttu-id="bf347-105">為了唯一識別 MCI 驅動程式，MCI 會使用 *裝置名稱*。</span><span class="sxs-lookup"><span data-stu-id="bf347-105">To uniquely identify an MCI driver, MCI uses *device names*.</span></span>

<span data-ttu-id="bf347-106">裝置名稱會在 SYSTEM.INI 檔案的 \[ mci \] 區段或登錄的適當部分中識別。</span><span class="sxs-lookup"><span data-stu-id="bf347-106">Device names are identified either in the \[mci\] section of the SYSTEM.INI file or in the appropriate part of the registry.</span></span> <span data-ttu-id="bf347-107">此資訊可識別 Windows 的所有 MCI 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="bf347-107">This information identifies all MCI drivers to Windows.</span></span> <span data-ttu-id="bf347-108">Mci 區段中的 \[ 專案 \] 使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="bf347-108">The entries in the \[mci\] section use the following form:</span></span>

<span data-ttu-id="bf347-109">*裝置 \_ 名稱*  =  *驅動程式 \_ 檔案名。副檔名*</span><span class="sxs-lookup"><span data-stu-id="bf347-109">*device\_name* = *driver\_filename.extension*</span></span>

<span data-ttu-id="bf347-110">下列範例顯示 SYSTEM.INI 的一般 \[ mci \] 區段：</span><span class="sxs-lookup"><span data-stu-id="bf347-110">The following example shows a typical \[mci\] section from SYSTEM.INI:</span></span>


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



<span data-ttu-id="bf347-111">如果使用 SYSTEM.INI 或登錄中已經存在的裝置名稱來安裝 MCI 驅動程式，系統會將整數附加至新驅動程式的裝置名稱，並建立唯一的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="bf347-111">If an MCI driver is installed using a device name that already exists in SYSTEM.INI or the registry, the system appends an integer to the device name of the new driver, creating a unique device name.</span></span> <span data-ttu-id="bf347-112">在上述範例中，使用 "cdaudio" 裝置名稱安裝的額外驅動程式將會被指派裝置名稱 "cdaudio1"。</span><span class="sxs-lookup"><span data-stu-id="bf347-112">In the preceding example, an additional driver installed using the "cdaudio" device name would be assigned the device name "cdaudio1".</span></span>

 

 




