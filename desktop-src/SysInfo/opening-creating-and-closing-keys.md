---
description: 應用程式必須先建立或開啟金鑰，應用程式才能將資料新增至登錄。
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: 開啟、建立和關閉索引鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970641"
---
# <a name="opening-creating-and-closing-keys"></a><span data-ttu-id="47b7b-103">開啟、建立和關閉索引鍵</span><span class="sxs-lookup"><span data-stu-id="47b7b-103">Opening, Creating, and Closing Keys</span></span>

<span data-ttu-id="47b7b-104">應用程式必須先建立或開啟金鑰，應用程式才能將資料新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="47b7b-104">Before an application can add data to the registry, it must create or open a key.</span></span> <span data-ttu-id="47b7b-105">若要建立或開啟金鑰，應用程式一律會將金鑰參考為目前開啟金鑰的子機碼。</span><span class="sxs-lookup"><span data-stu-id="47b7b-105">To create or open a key, an application always refers to the key as a subkey of a currently open key.</span></span> <span data-ttu-id="47b7b-106">下列預先定義的金鑰一律會開啟 **： HKEY \_ 本機 \_ 電腦**、 **HKEY \_ 類別 \_ 根**、 **HKEY \_ 使用者**，以及 **HKEY 目前的 \_ \_ 使用者**。</span><span class="sxs-lookup"><span data-stu-id="47b7b-106">The following predefined keys are always open: **HKEY\_LOCAL\_MACHINE**, **HKEY\_CLASSES\_ROOT**, **HKEY\_USERS**, and **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="47b7b-107">應用程式會使用 [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) 函數來開啟索引鍵，並使用 [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) 函式來建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="47b7b-107">An application uses the [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) function to open a key and the [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) function to create a key.</span></span> <span data-ttu-id="47b7b-108">登錄樹狀目錄可以是深512層級。</span><span class="sxs-lookup"><span data-stu-id="47b7b-108">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="47b7b-109">您可以透過單一登入 API 呼叫，一次最多建立32個層級。</span><span class="sxs-lookup"><span data-stu-id="47b7b-109">You can create up to 32 levels at a time through a single registry API call.</span></span>

<span data-ttu-id="47b7b-110">應用程式可以使用 [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) 函式來關閉機碼，並將其包含的資料寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="47b7b-110">An application can use the [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) function to close a key and write the data it contains into the registry.</span></span> <span data-ttu-id="47b7b-111">**RegCloseKey** 不一定會在傳回之前將資料寫入登錄;將快取排清至硬碟可能需要數秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="47b7b-111">**RegCloseKey** does not necessarily write the data to the registry before returning; it can take as much as several seconds for the cache to be flushed to the hard disk.</span></span> <span data-ttu-id="47b7b-112">如果應用程式必須明確地將登錄資料寫入硬碟，則可以使用 [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) 函數。</span><span class="sxs-lookup"><span data-stu-id="47b7b-112">If an application must explicitly write registry data to the hard disk, it can use the [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) function.</span></span> <span data-ttu-id="47b7b-113">不過， **RegFlushKey** 會使用許多系統資源，而且只有在絕對必要時才應該呼叫。</span><span class="sxs-lookup"><span data-stu-id="47b7b-113">**RegFlushKey**, however, uses many system resources and should be called only when absolutely necessary.</span></span>

 

 



