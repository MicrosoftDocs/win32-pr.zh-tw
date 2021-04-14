---
title: 安裝範例提供者元件
description: 安裝 ADSI SDK 之後，請從安裝目錄將目錄變更為範例 \\ NetDs \\ ADSI \\ 範例 \\ 提供者 \\ 安裝子目錄。 執行 Install.bat，如 README.TXT 檔中所述。
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- 安裝範例提供者元件 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0df567aa08b03ce9c043d345380f05cd6d1c20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371841"
---
# <a name="installing-the-example-provider-component"></a><span data-ttu-id="46f5a-105">安裝範例提供者元件</span><span class="sxs-lookup"><span data-stu-id="46f5a-105">Installing the Example Provider Component</span></span>

<span data-ttu-id="46f5a-106">安裝 ADSI SDK 之後，請從安裝目錄將目錄變更為範例 \\ NetDs \\ ADSI \\ 範例 \\ 提供者 \\ 安裝子目錄。</span><span class="sxs-lookup"><span data-stu-id="46f5a-106">After installing the ADSI SDK, from the installation directory, change directories to the Samples\\NetDs\\ADSI\\Samples\\Provider\\Setup subdirectory.</span></span> <span data-ttu-id="46f5a-107">執行 Install.bat，如 README.TXT 檔中所述。</span><span class="sxs-lookup"><span data-stu-id="46f5a-107">Run Install.bat as described in the README.TXT file.</span></span>

<span data-ttu-id="46f5a-108">範例 ADSI 提供者會在執行 Install.bat 檔案時，將下列子機碼和值新增至登錄：</span><span class="sxs-lookup"><span data-stu-id="46f5a-108">The sample ADSI provider will add the following subkeys and values to the registry when Install.bat file is run:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               Sample = SampleNamespace
```

```
HKEY_CLASSES_ROOT
   SampleNamespace
      Clsid = {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   Sample
      Clsid = {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Namespace Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = SampleNamespace
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Provider Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = Sample
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

<span data-ttu-id="46f5a-109">範例提供者元件的其他登錄專案存在，是因為範例提供者元件在登錄中已執行其目錄階層。</span><span class="sxs-lookup"><span data-stu-id="46f5a-109">Other registry entries for the example provider component exist because the example provider component implemented its directory hierarchy in the registry.</span></span> <span data-ttu-id="46f5a-110">如此一來，就不會暗示其他提供者想要或應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="46f5a-110">This in no way implies other providers would want to or should do the same.</span></span>

 

 




