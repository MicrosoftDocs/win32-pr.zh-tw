---
description: 說明如何使用 Shell 動詞命令叫用 DDE 命令。
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: 如何建立動詞與 DDE 命令的關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973176"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a><span data-ttu-id="f4f09-103">如何建立動詞與 DDE 命令的關聯</span><span class="sxs-lookup"><span data-stu-id="f4f09-103">How to Associate Verbs with DDE Commands</span></span>

<span data-ttu-id="f4f09-104">叫用動詞通常會啟動動詞命令子機碼所指定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f4f09-104">Invoking a verb ordinarily launches the application that is specified by the verb's command subkey.</span></span> <span data-ttu-id="f4f09-105">但是，如果您的應用程式支援動態資料交換 (的 DDE) ，則可以改為讓 Shell 起始 DDE 交談。</span><span class="sxs-lookup"><span data-stu-id="f4f09-105">However, if your application supports Dynamic Data Exchange (DDE), you can instead have the Shell initiate a DDE conversation.</span></span>

<span data-ttu-id="f4f09-106">若要指定叫用動詞應該起始 DDE 交談，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="f4f09-106">To specify that invoking a verb should initiate a DDE conversation, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="f4f09-107">指示</span><span class="sxs-lookup"><span data-stu-id="f4f09-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="f4f09-108">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="f4f09-108">Step 1:</span></span>

<span data-ttu-id="f4f09-109">將 **ddeexec** 子機碼新增至動詞的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f4f09-109">Add a **ddeexec** subkey to the verb's key.</span></span>

### <a name="step-2"></a><span data-ttu-id="f4f09-110">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="f4f09-110">Step 2:</span></span>

<span data-ttu-id="f4f09-111">將 **ddeexec** 的預設值設定為 [DDE 命令字串]。</span><span class="sxs-lookup"><span data-stu-id="f4f09-111">Set the default value of **ddeexec** to the DDE command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f09-112">備註</span><span class="sxs-lookup"><span data-stu-id="f4f09-112">Remarks</span></span>

<span data-ttu-id="f4f09-113">**Ddeexec** 索引鍵有三個選擇性子機碼，可讓您控制 DDE 進程：</span><span class="sxs-lookup"><span data-stu-id="f4f09-113">The **ddeexec** key has three optional subkeys that provide some control over the DDE process:</span></span>

-   <span data-ttu-id="f4f09-114">**應用程式**。</span><span class="sxs-lookup"><span data-stu-id="f4f09-114">**application**.</span></span> <span data-ttu-id="f4f09-115">將此子機碼的預設值設定為要用來建立 DDE 交談的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f4f09-115">Set the default value of this subkey to the application name to be used to establish the DDE conversation.</span></span> <span data-ttu-id="f4f09-116">如果沒有 **應用程式** 子機碼，則會使用動詞 **命令** 子機碼的預設值做為應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f4f09-116">If there is no **application** subkey, the default value of the verb's **command** subkey is used as the application name.</span></span>
-   <span data-ttu-id="f4f09-117">**主題**。</span><span class="sxs-lookup"><span data-stu-id="f4f09-117">**topic**.</span></span> <span data-ttu-id="f4f09-118">將此子機碼的預設值設定為 DDE 交談的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="f4f09-118">Set the default value of this subkey to the topic name of the DDE conversation.</span></span> <span data-ttu-id="f4f09-119">如果沒有 **主題** 子機碼，則會使用 System 做為主題名稱。</span><span class="sxs-lookup"><span data-stu-id="f4f09-119">If there is no **topic** subkey, System is used as the topic name.</span></span>
-   <span data-ttu-id="f4f09-120">**ifexec**。</span><span class="sxs-lookup"><span data-stu-id="f4f09-120">**ifexec**.</span></span> <span data-ttu-id="f4f09-121">將此子機碼的預設值設定為當無法起始 DDE 交談時要使用的 DDE 命令。</span><span class="sxs-lookup"><span data-stu-id="f4f09-121">Set the default value of this subkey to the DDE command to be used if DDE conversation cannot be initiated.</span></span> <span data-ttu-id="f4f09-122">當初始化失敗時，會啟動由動詞 **命令** 子機碼的預設值所指定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f4f09-122">When initiation fails, the application that is specified by the default value of the verb's **command** subkey is launched.</span></span> <span data-ttu-id="f4f09-123">如果有 **ifexec** 索引鍵，則會使用預設值作為 DDE 命令。</span><span class="sxs-lookup"><span data-stu-id="f4f09-123">If an **ifexec** key exists, its default value will then be used as the DDE command.</span></span> <span data-ttu-id="f4f09-124">如果沒有 **ifexec** 子機碼，則會再次使用 **ddeexec** 索引鍵的預設值做為 DDE 命令。</span><span class="sxs-lookup"><span data-stu-id="f4f09-124">If there is no **ifexec** subkey, the default value of the **ddeexec** key will be used again as the DDE command.</span></span>

<span data-ttu-id="f4f09-125">下列範例會指定叫用 Myprogram.exe 的 open 動詞命令，並使用 Open ( "%1" ) 的 DDE 命令和應用程式名稱 Myprogram.exe 來起始 DDE 交談。</span><span class="sxs-lookup"><span data-stu-id="f4f09-125">The following example specifies that invoking the open verb for MyProgram.1 initiates a DDE conversation with a DDE command of Open("%1") and an application name of MyProgram.</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



