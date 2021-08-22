---
description: 完成提供者的 WMI 之後，它會從記憶體卸載提供者。
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: 卸載提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b831f69ba27ab3e173920cc57e7500ef543bb327a04dc5c04dc8b0b9cef31ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049956"
---
# <a name="unloading-a-provider"></a>卸載提供者

完成提供者的 WMI 之後，它會從記憶體卸載提供者。 WMI 卸載提供者的主要原因是要節省系統資源。 因此，您必須新增可讓 WMI 以有效率的方式卸載提供者的程式碼。 它會從快取控制項指定的間隔時間，到 WMI 要卸載提供者的間隔兩倍。

WMI 會以下列其中一種方式卸載提供者：

-   在提供者完成提供給它的工作之後，請將提供者卸載。
-   當使用者關閉系統時，快速卸載所有提供者。 請注意，WMI 服務從命令列關閉時，WMI 會卸載同進程提供者。

雖然第一個案例較常見，但您必須撰寫您的提供者以瞭解這兩種可能性。

本主題將討論下列各節：

-   [卸載閒置提供者](#unloading-an-idle-provider)
-   [存取提供者的閒置時間](#accessing-the-idle-time-for-a-provider)
-   [卸載也是 WMI 用戶端的提供者](#unloading-a-provider-that-is-also-a-wmi-client)
-   [在關機期間卸載提供者](#unloading-a-provider-during-shutdown)
-   [相關主題](#related-topics)

## <a name="unloading-an-idle-provider"></a>卸載閒置提供者

WMI 卸載閒置提供者時，會執行下列動作：

-   判斷提供者是否閒置。

    WMI 會使用 **ClearAfter** 屬性來決定提供者在卸載該提供者之前，可保持閒置的時間長度。 如需詳細資訊，請參閱 [存取提供者的閒置時間](#accessing-the-idle-time-for-a-provider)。

-   呼叫提供者的 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法。

    如果提供者是純服務提供者，則 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 會從使用中的記憶體中完全移除提供者。 不過，nonpure 提供者可能會在 WMI 呼叫 **發行** 之後繼續執行。

## <a name="accessing-the-idle-time-for-a-provider"></a>存取提供者的閒置時間

提供者保持作用中的最小時間量是由 **ClearAfter** 屬性所決定。 您可以在根命名空間中衍生自 WMI 系統類別 [**\_ \_ CacheControl**](--cachecontrol.md)的類別實例中，找到 **ClearAfter** \\ 。

下列清單描述衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)的類別，此類別會控制提供者卸載：

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

您可以針對特定類型的提供者，在快取控制項實例中編輯 **ClearAfter** 屬性，以變更 WMI 允許提供者保持非使用中的最小時間量。 例如，若要限制屬性提供者可以維持閒置的時間量，您可以在根命名空間中編輯 [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)實例的 **ClearAfter** 屬性 \\ 。

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>卸載也是 WMI 用戶端的提供者

當您的提供者完成呼叫的提供者函式之後，可能需要保持 WMI 的用戶端。 例如，推送提供者可能需要向 WMI 發出查詢。 如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。 在此情況下，表示提供者之 [**\_ \_ Win32Provider**](--win32provider.md)實例的 **純** 屬性應該設定為 **TRUE**。 如果 **純** 屬性設為 **FALSE**，則當 WMI 呼叫其主要介面的發行方法時，提供者會在所有未完成的介面點上呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，藉以準備卸載。 如需詳細資訊，請參閱 [**\_ \_ Win32Provider**](--win32provider.md)中的「備註」一節。

下列程式描述如何針對提供者的主要介面來執行發行方法。

**若要卸載提供者**

1.  當 WMI 呼叫您提供者主要介面的 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法時，釋放針對 wmi 所持有的所有介面指標。

    一般而言，提供者會保留 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)中提供的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)和 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)介面的指標。

2.  如果相關聯的 [**\_ \_ Win32Provider**](--win32provider.md)實例中的 **Pure** 屬性設定為 **FALSE**，則提供者可以在 WMI 呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)之後轉換至用戶端應用程式的角色。 不過，WMI 無法卸載以用戶端系統的形式運作的提供者，這會增加系統的額外負荷。

    **純** 設為 **TRUE** 的提供者只存在於服務要求。 因此，這種類型的提供者無法採用用戶端應用程式的角色，而且 WMI 可以將它卸載。

## <a name="unloading-a-provider-during-shutdown"></a>在關機期間卸載提供者

在一般情況下，使用卸載 [也是 Wmi 用戶端的提供者](#unloading-a-provider-that-is-also-a-wmi-client) 的指導方針，可讓 wmi 適當地卸載您的提供者。 不過，您可能會遇到 WMI 無法 instigate 一般卸載程式的情況，例如，當使用者選擇關閉系統時。 藉由使用資料儲存體的交易模型，除了執行良好的清除策略之外，您還可以確定您的提供者已正確卸載。

使用者可以隨時停止 WMI。 在這種情況下，WMI 不會卸載任何提供者，也不會在任何同進程提供者上呼叫 [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) 進入點。 此外，如果同進程提供者是在關機時的方法呼叫中間，WMI 可能會在呼叫的中間終止執行中的執行緒。 在此情況下，WMI 不會呼叫通常會處理清除的常式，例如物件的函式。 WMI 最多隻會呼叫 [**DllMain**](/windows/desktop/Dlls/dllmain) 。

當作業系統關閉 WMI 時，系統會自動釋放配置給同進程提供者的所有記憶體。 作業系統也會關閉提供者所持有的大部分資源，例如檔案控制代碼、視窗控制碼等等。 提供者不需要採取任何特定動作來進行這種動作。

因為 WMI 可能會在呼叫中間關機，所以提供者不應讓資料來源處於不一致的狀態。 讓您的資料處於不一致的狀態，並不是唯讀提供者的問題。 不過，具有寫入功能的提供者可能會想要在突然終止之後，執行某種類型的交易模型，以允許安全的回復。

雖然作業系統可能會釋放一些一般系統資源，但系統並不會自動釋放所有資源。 例如，作業系統可能無法釋放通訊端或資料庫連接。 相反地，提供者可能需要手動清除這類資源。 若要避免這些問題，您可以跨進程執行您的提供者，也可以加入清除程式碼。

最簡單的解決方案是跨進程執行您的提供者。 當 WMI 關機時，不會終止跨進程提供者，雖然 WMI 將在 COM timeout 之後釋放該提供者。 清除和終止強大問題的提供者，比效能可能跨進程更重要。

如果您必須將清除程式碼放在您的提供者中，您有兩個選項。 執行這類清除的一個地方就是 [**DllMain**](/windows/desktop/Dlls/dllmain)，在卸載 dll 時，作業系統會呼叫 dll 進入點函數。 清除程式碼可以直接加入 **DllMain** 中，執行它以回應 **DLL 進程 \_ 卸 \_ 離**。 在 **DllMain** 中執行清除程式碼可能有點困難，尤其是在 MFC 或 ATL 之類的程式設計環境中。 For more information, see the Microsoft Knowledge Base article Q148791, "*How to Provide Your Own DllMain in an MFC Regular DLL.*"  (此資源可能無法在某些語言及國家或地區使用。 ) 

或者，您也可以將清除程式碼放在全域類別的函式中。 如需詳細資訊，請參閱卸載提供者。 Windows 作業系統不會在堆積上配置全域物件。 相反地，作業系統會在 DLL 卸載期間呼叫析構函數。

以下是一個簡單的清除程式，可容納于 WMI 的全域物件內。


```C++
class CMyCleanup
{
    ~CMyCleanup()
    {
        CloseHandle(m_hOpenFile);
        CloseDatabaseConnection(g_hDatabase);
    }
} g_Cleanup;
```



使用任一種方法可在清除程式碼中完成的工作有許多限制。 例如，不會以任何方式存取未隱含連結的執行緒和任何 Dll。 此外，您無法在任何情況下進行 COM 呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> </dl>

 

 
