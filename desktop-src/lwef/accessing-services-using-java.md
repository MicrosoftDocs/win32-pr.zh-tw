---
title: 使用 JAVA 存取服務
description: 使用 JAVA 存取服務
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19a9a3feb1e6cb5fc9ddb8a24b87adfdb42461ebb4581723c1cdb465739c51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976848"
---
# <a name="accessing-services-using-java"></a>使用 JAVA 存取服務

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

您也可以從 JAVA applet 存取 Microsoft Agent 服務。 許多可透過 Microsoft Agent 介面存取的函式會透過傳址方式傳遞的參數傳回值。 若要從 JAVA 傳遞這些參數，您必須在程式碼中建立單一元素的陣列，並將它們以參數形式傳遞給適當的函式。 如果您使用 Microsoft Visual c + +，並已在 Microsoft 代理程式伺服器上執行 JAVA 類型程式庫嚮導，請參閱 summary.txt 檔案，以檢查哪些函數需要陣列引數。 程式與 C 中的程式類似;您可以使用 [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) 介面來建立伺服器的實例，然後載入該字元：


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



從 HTTP 遠端位置（例如網站）載入字元時，此程式會稍有不同。 在此情況下， [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) 方法是非同步，而且會引發 E \_ 暫止 (0X8000000A) 的 COM 例外狀況。 您將需要攔截此例外狀況，並正確地處理它，就像在下列函式中所做的一樣：


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



然後取得可讓您存取其方法的 [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) 介面：


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



同樣地，若要收到事件的通知，您必須執行 [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) 或 [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) 介面，建立並註冊該型別的物件：


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



若要從 JAVA applet 存取 Microsoft 代理程式，您必須產生使用 applet 安裝的 JAVA 類別。 例如，您可以使用 Visual j + + JAVA 類型程式庫 Wizard 來產生這些檔案。 如果您想要在網頁上裝載小程式，您必須建立一個帶正負號的 JAVA CAB，內含隨頁面下載的產生類別檔案。 需要類別檔案才能存取 Microsoft 代理程式伺服器，因為它是在 JAVA 沙箱外部執行的 COM 物件。 若要深入瞭解 JAVA 的 Trust-Based 安全性，請參閱 <https://www.microsoft.com/java/security> 。

 

 