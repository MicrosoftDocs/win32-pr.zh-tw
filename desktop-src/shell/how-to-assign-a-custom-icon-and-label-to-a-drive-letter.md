---
description: 指定磁片磁碟機的自訂圖示和標籤。
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: 將自訂圖示和標籤指派給磁碟機號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973188"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a><span data-ttu-id="2ff2c-103">如何將自訂圖示和標籤指派給磁碟機號</span><span class="sxs-lookup"><span data-stu-id="2ff2c-103">How to Assign a Custom Icon and Label to a Drive Letter</span></span>

<span data-ttu-id="2ff2c-104">指定磁片磁碟機的自訂圖示和標籤。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-104">Specify a custom icon and label for a drive.</span></span>

## <a name="instructions"></a><span data-ttu-id="2ff2c-105">指示</span><span class="sxs-lookup"><span data-stu-id="2ff2c-105">Instructions</span></span>

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a><span data-ttu-id="2ff2c-106">步驟1：以 Windows 2000 中的自訂圖示取代標準磁片磁碟機圖示</span><span class="sxs-lookup"><span data-stu-id="2ff2c-106">Step 1: Replacing the standard drive icon with a custom icon in Windows 2000</span></span>

<span data-ttu-id="2ff2c-107">若要以 Windows 2000 中的自訂圖示取代標準磁片磁碟機圖示，請將磁碟機號命名的子機碼新增至下列機碼。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-107">To replace the standard drive icon with a custom icon in Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

<span data-ttu-id="2ff2c-108">下列範例會指定 E：磁片磁碟機的自訂圖示和標籤。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-108">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="2ff2c-109">此圖示位於 C： \\ MyDirMyDrive.exe 檔案中 \\ ，以零為基底的索引為三個。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-109">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="2ff2c-110">若為 Windows 2000：</span><span class="sxs-lookup"><span data-stu-id="2ff2c-110">For Windows 2000:</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a><span data-ttu-id="2ff2c-111">步驟2：以所有其他 Windows 版本的自訂圖示取代標準磁片磁碟機圖示</span><span class="sxs-lookup"><span data-stu-id="2ff2c-111">Step 2: Replacing the standard drive icon with a custom icon in all other versions of Windows</span></span>

<span data-ttu-id="2ff2c-112">若要以 Windows 2000 以外的所有 Windows 版本中的自訂圖示取代標準磁片磁碟機圖示，請將磁碟機號命名的子機碼新增至下列機碼。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-112">To replace the standard drive icon with a custom icon in all versions of Windows other than Windows 2000, add a subkey named for the drive letter to the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

<span data-ttu-id="2ff2c-113">下列範例會指定 E：磁片磁碟機的自訂圖示和標籤。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-113">The following example specifies a custom icon and label for the E: drive.</span></span> <span data-ttu-id="2ff2c-114">此圖示位於 C： \\ MyDirMyDrive.exe 檔案中 \\ ，以零為基底的索引為三個。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-114">The icon is in the C:\\MyDir\\MyDrive.exe file with a zero-based index of three.</span></span>

<span data-ttu-id="2ff2c-115">針對所有其他版本的 Windows：</span><span class="sxs-lookup"><span data-stu-id="2ff2c-115">For all other versions of Windows:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a><span data-ttu-id="2ff2c-116">步驟3：呼叫 SHUpdateImage 事件</span><span class="sxs-lookup"><span data-stu-id="2ff2c-116">Step 3: Calling the SHUpdateImage Event</span></span>

<span data-ttu-id="2ff2c-117">在所有版本的 Windows 中，如果您變更檔案類型或磁片磁碟機圖示，您也必須呼叫 SHUpdateImage 來通知 Shell 更新目前顯示的任何圖示。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-117">In all versions of Windows, if you change a file type or drive icon you must also call SHUpdateImage to notify the Shell to update any icons that are currently displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff2c-118">備註</span><span class="sxs-lookup"><span data-stu-id="2ff2c-118">Remarks</span></span>

<span data-ttu-id="2ff2c-119">磁碟機號後面不能加上冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-119">The drive letter should not be followed by a colon (:).</span></span> <span data-ttu-id="2ff2c-120">將 **DefaultIcon** 子機碼新增至磁碟機號子機碼，並將其預設值設定為包含圖示位置的字串。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-120">Add a **DefaultIcon** subkey to the drive letter subkey and set its default value to a string that contains the location of the icon.</span></span> <span data-ttu-id="2ff2c-121">字串的第一個部分包含圖示檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-121">The first part of the string contains the fully-qualified path of the icon's file.</span></span> <span data-ttu-id="2ff2c-122">如果檔案中有一個以上的圖示，路徑後面會接著逗號，然後是以零為基底的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="2ff2c-122">If there is more than one icon in the file, the path is followed by a comma, and then by the zero-based index of the icon.</span></span>

 

 



