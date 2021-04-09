---
title: 在 DLL 中建立 File-Handler 實例
description: 在 DLL 中建立 File-Handler 實例
ms.assetid: 0cf7ef72-c675-4a67-97b3-18cccfb7ddc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95a462d9c2f56abb5985904c4acc1fb12d10877
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682108"
---
# <a name="creating-a-file-handler-instance-in-a-dll"></a><span data-ttu-id="06114-103">在 DLL 中建立 File-Handler 實例</span><span class="sxs-lookup"><span data-stu-id="06114-103">Creating a File-Handler Instance in a DLL</span></span>

<span data-ttu-id="06114-104">當應用程式指定您的檔案處理常式 DLL 或串流處理常式時，系統會依其類別識別碼在登錄中尋找並載入。</span><span class="sxs-lookup"><span data-stu-id="06114-104">When an application specifies your file-handler DLL or stream handler, the system looks it up in the registry by its class identifier and loaded.</span></span> <span data-ttu-id="06114-105">系統接著會呼叫 DLL 的 [**DllGetClassObject**](/previous-versions//dd797891(v=vs.85)) 函式，以建立檔案或資料流程處理常式的實例。</span><span class="sxs-lookup"><span data-stu-id="06114-105">The system then calls the [**DllGetClassObject**](/previous-versions//dd797891(v=vs.85)) function of the DLL to create an instance of the file or stream handler.</span></span> <span data-ttu-id="06114-106">下列 (以 c + + 撰寫的範例) 顯示檔案處理常式如何建立實例。</span><span class="sxs-lookup"><span data-stu-id="06114-106">The following example (written in C++) shows how a file handler creates an instance.</span></span>


```C++
// Main DLL entry point. 
STDAPI DllGetClassObject(const CLSID FAR& rclsid, 
    const IID FAR& riid, void FAR* FAR* ppv) 
{ 
    HRESULT hresult; 
    hresult = CAVIFileCF::Create(rclsid, riid, ppv); 
    return hresult; 
} 
HRESULT CAVIFileCF::Create(const CLSID FAR&   rclsid, 
    const IID FAR& riid, void FAR* FAR*   ppv) 
{ 
// The following is the class factory creation and not an 
// actual PAVIFile. 
    CAVIFileCF FAR*   pAVIFileCF; 
    IUnknown FAR*   pUnknown; 
    HRESULT hresult; 
 
// Create the instance. 
    pAVIFileCF = new FAR CAVIFileCF(rclsid, &pUnknown); 
    if (pAVIFileCF == NULL) 
        return ResultFromScode(E_OUTOFMEMORY); 
 
// Set the interface pointer. 
    hresult = pUnknown->QueryInterface(riid, ppv); 
    if (FAILED(GetScode(hresult))) 
        delete pAVIFileCF; 
    return hresult; 
} 

```



 

 