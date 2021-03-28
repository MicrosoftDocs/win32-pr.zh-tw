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
# <a name="how-to-associate-verbs-with-dde-commands"></a>如何建立動詞與 DDE 命令的關聯

叫用動詞通常會啟動動詞命令子機碼所指定的應用程式。 但是，如果您的應用程式支援動態資料交換 (的 DDE) ，則可以改為讓 Shell 起始 DDE 交談。

若要指定叫用動詞應該起始 DDE 交談，請遵循下列步驟。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

將 **ddeexec** 子機碼新增至動詞的金鑰。

### <a name="step-2"></a>步驟 2:

將 **ddeexec** 的預設值設定為 [DDE 命令字串]。

## <a name="remarks"></a>備註

**Ddeexec** 索引鍵有三個選擇性子機碼，可讓您控制 DDE 進程：

-   **應用程式**。 將此子機碼的預設值設定為要用來建立 DDE 交談的應用程式名稱。 如果沒有 **應用程式** 子機碼，則會使用動詞 **命令** 子機碼的預設值做為應用程式名稱。
-   **主題**。 將此子機碼的預設值設定為 DDE 交談的主題名稱。 如果沒有 **主題** 子機碼，則會使用 System 做為主題名稱。
-   **ifexec**。 將此子機碼的預設值設定為當無法起始 DDE 交談時要使用的 DDE 命令。 當初始化失敗時，會啟動由動詞 **命令** 子機碼的預設值所指定的應用程式。 如果有 **ifexec** 索引鍵，則會使用預設值作為 DDE 命令。 如果沒有 **ifexec** 子機碼，則會再次使用 **ddeexec** 索引鍵的預設值做為 DDE 命令。

下列範例會指定叫用 Myprogram.exe 的 open 動詞命令，並使用 Open ( "%1" ) 的 DDE 命令和應用程式名稱 Myprogram.exe 來起始 DDE 交談。

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

 

 



