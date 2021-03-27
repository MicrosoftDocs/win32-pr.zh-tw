---
description: 說明如何確保您的應用程式會出現在桌面應用程式的 [開啟方式] 功能表和對話方塊中，並以預設的 Windows Store 應用程式的形式提供給指定的檔案類型。
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: 如何在 [開啟方式] 對話方塊中加入應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849193"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a><span data-ttu-id="00d98-103">如何在 [開啟方式] 對話方塊中加入應用程式</span><span class="sxs-lookup"><span data-stu-id="00d98-103">How to Include an Application in the Open With Dialog Box</span></span>

<span data-ttu-id="00d98-104">說明如何確保您的應用程式會出現在桌面應用程式的 [ **開啟方式** ] 功能表和對話方塊中，並以預設的 Windows Store 應用程式的形式提供給指定的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="00d98-104">Illustrates how to ensure your application appears in the **Open With** menu and dialog box for desktop apps, and is available as a default Windows Store app for specified file types.</span></span>

## <a name="instructions"></a><span data-ttu-id="00d98-105">指示</span><span class="sxs-lookup"><span data-stu-id="00d98-105">Instructions</span></span>

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a><span data-ttu-id="00d98-106">針對每個檔案類型，將您的應用程式新增至 OpenWithProgIds 登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="00d98-106">For each file type, add your application to the OpenWithProgIds registry subkey.</span></span>

<span data-ttu-id="00d98-107">新增您的 ProgID 作為值名稱，並以 REG \_ NONE 或 reg SZ 的數值型別， \_ 以及空字串作為資料值。</span><span class="sxs-lookup"><span data-stu-id="00d98-107">Add your ProgID as a value name, with the value type of either REG\_NONE or REG\_SZ and an empty string as the data value.</span></span>

<span data-ttu-id="00d98-108">下列登錄範例會顯示與 InfoPath 相關聯的專案，以及具有 XML 檔案類型的 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="00d98-108">The following registry examples show entries associating InfoPath and for Microsoft Visual Studio with the XML file type.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a><span data-ttu-id="00d98-109">備註</span><span class="sxs-lookup"><span data-stu-id="00d98-109">Remarks</span></span>

<span data-ttu-id="00d98-110">**OpenWithProgids** 子機碼優先于 **OpenWithList** 以識別應用程式。</span><span class="sxs-lookup"><span data-stu-id="00d98-110">The **OpenWithProgids** subkey is preferred to **OpenWithList** to identify an application.</span></span> <span data-ttu-id="00d98-111">如需這些子機碼的詳細資訊，請參閱設定選用子機碼 [和檔案類型延伸模組屬性](fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="00d98-111">For more information on these subkeys, see [Setting Optional Subkeys and File Type Extension Attributes](fa-file-types.md).</span></span>

<span data-ttu-id="00d98-112">**OpenWithList** 僅適用于繼承應用程式 (只有在 Windows XP 之前的作業系統上才必須) .exe。</span><span class="sxs-lookup"><span data-stu-id="00d98-112">**OpenWithList** is intended only for legacy apps (must be .exe only) on operating systems prior to Windows XP.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



