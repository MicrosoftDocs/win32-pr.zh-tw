---
title: InprocServer32
description: 註冊32位的同進程伺服器，並指定伺服器可以在其中執行之單元的執行緒模型。
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9904aa636bbfb8dc0bc01cac85e041aedfcd34364bd62ac7b0e4e5a9f904750f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567818"
---
# <a name="inprocserver32"></a>InprocServer32

註冊32位的同進程伺服器，並指定伺服器可以在其中執行之單元的執行緒模型。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>備註

**>Threadingmodel** 是指定執行緒模型的 **REG \_ SZ** 值。 下表顯示可能的值。



| 值     | 描述                                |
|-----------|--------------------------------------------|
| 公寓 | 單一執行緒單元                  |
| 兩者      | 單一執行緒或多執行緒單元 |
| 免費      | 多執行緒單元                    |
| 中性   | 中立的單元                          |



 

同進程伺服器所提供的每個物件都必須使用相同的值。

如果 **>threadingmodel** 不存在或未設定為值，則會將伺服器載入至在進程中初始化的第一個單元。 此單元有時稱為主要單一執行緒的單元 (STA) 。 如果進程中的第一個 STA 是由 COM 初始化，而不是明確呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)，就稱為主機 STA。 例如，如果要載入的內含式伺服器需要 STA 但進程中目前沒有 STA，COM 就會建立主機 STA。

在可能的情況下，同進程伺服器會載入至載入它的用戶端所在的相同單元中。 如果用戶端單元的執行緒模型與指定的模型不相容，則會載入伺服器，如下表所示。



| 伺服器的執行緒模型 | 執行中的單元伺服器 |
|---------------------------|----------------------------|
| <not specified>     | 主要 STA                   |
| 兩者                      | 與用戶端相同的單元   |
| 免費                      | 多執行緒單元    |
| 中性                   | 中立的單元          |



 

如果伺服器的執行緒模型為「單元」，則載入伺服器的單元取決於用戶端執行所在的部門，如下表所示。



| 執行中的單元用戶端 | 執行中的單元伺服器 |
|----------------------------|----------------------------|
| 多執行緒              | 主機 STA                   |
| STA 執行緒上的中性 ()     | 與用戶端相同的單元   |
| MTA 執行緒上的中性 ()     | 主機 STA                   |



 

COM 也可以建立主控制項多執行緒單元 (MTA) 。 如果單一執行緒中的用戶端要求執行緒模型在進程中沒有 MTA 時為可用的同進程伺服器，COM 會建立主機 MTA 並將伺服器載入其中。

若為32位的同進程伺服器，則必須註冊 [**InprocHandler32**](inprochandler32.md)、 [**InprocServer**](inprocserver.md)、 **InprocServer32** 和可 [**插入**](insertable.md) 的索引鍵。 **InprocServer** 專案只是為了回溯相容性所需。 如果遺漏，類別仍可運作，但無法在16位應用程式中載入。

如果容器正在搜尋內含式伺服器的登錄，16位版本的優先順序會和16位容器相同，且32位版本的優先順序會與32位容器相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




