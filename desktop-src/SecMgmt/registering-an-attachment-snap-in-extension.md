---
description: 建立附件嵌入式管理單元擴充功能之後，您必須註冊它，MMC 和安全性設定嵌入式管理單元才能找到並使用它。
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: 註冊附件嵌入式管理單元延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970789"
---
# <a name="registering-an-attachment-snap-in-extension"></a><span data-ttu-id="f5bb2-103">註冊附件嵌入式管理單元延伸模組</span><span class="sxs-lookup"><span data-stu-id="f5bb2-103">Registering an Attachment Snap-in Extension</span></span>

<span data-ttu-id="f5bb2-104">建立附件嵌入式管理單元擴充功能之後，您必須註冊它，MMC 和安全性設定嵌入式管理單元才能找到並使用它。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-104">After you create an attachment snap-in extension, you must register it in order for the MMC and the Security Configuration snap-ins to locate and use it.</span></span>

<span data-ttu-id="f5bb2-105">您的附件嵌入式管理單元必須藉由新增自己的節點來擴充安全性設定嵌入式管理單元命名空間，如下列程式所述。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-105">Your attachment snap-in must extend the Security Configuration snap-ins namespace by adding its own node as described in the following procedure.</span></span>

<span data-ttu-id="f5bb2-106">**安裝並註冊附件嵌入式管理單元延伸模組**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-106">**To install and register the attachment snap-in extension**</span></span>

1.  <span data-ttu-id="f5bb2-107">在下列登錄機碼下註冊嵌入式管理單元延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-107">Register the snap-in extension under the following registry key.</span></span> <span data-ttu-id="f5bb2-108">請勿在嵌入式管理單元下建立獨立金鑰;附件嵌入式管理單元延伸模組必須是延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-108">Do not create a StandAlone key under the snap-in; attachment snap-ins extensions must only be extensions.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  <span data-ttu-id="f5bb2-109">在下列子機碼下註冊附件嵌入式管理單元延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-109">Register the attachment snap-in extension under the following subkeys.</span></span> <span data-ttu-id="f5bb2-110">這可做為 **DllRegisterServer** 和 **DllUnregisterServer** 函式執行的一部分。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-110">This can be done as part of your **DllRegisterServer** and **DllUnregisterServer** function implementations.</span></span>

    <span data-ttu-id="f5bb2-111">[安全性範本](security-templates.md) 命名空間：</span><span class="sxs-lookup"><span data-stu-id="f5bb2-111">[Security Templates](security-templates.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    <span data-ttu-id="f5bb2-112">[安全性設定與分析](security-configuration-and-analysis.md) 命名空間：</span><span class="sxs-lookup"><span data-stu-id="f5bb2-112">[Security Configuration and Analysis](security-configuration-and-analysis.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



