---
title: 系統管理通知處理常式
description: Microsoft Active Directory 消費者和電腦 MMC 嵌入式管理單元提供一種機制，可讓元件在使用者刪除、重新命名、移動或變更物件的屬性時，使用嵌入式管理單元來接收通知。
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- 系統管理通知處理常式廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d89627cdb15cc7ea15f4b56e3a6ec90eafbe6a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879883"
---
# <a name="administrative-notification-handlers"></a>系統管理通知處理常式

Microsoft Active Directory 消費者和電腦 MMC 嵌入式管理單元提供一種機制，可讓元件在使用者刪除、重新命名、移動或變更物件的屬性時，使用嵌入式管理單元來接收通知。 接收通知的元件稱為「通知處理常式」。

當多個物件連結在一起，且必須存在於相同的容器內時，這會很有用。 如果移動其中一個連結化物件，則會提供通知處理常式的通知，而通知處理常式可以將其他連結的物件移至相同的資料夾。

當執行其中一項作業並安裝一或多個通知處理常式時，[使用者和電腦] 嵌入式管理單元會顯示確認對話方塊，其中會列出通知處理常式，以及每個處理常式的核取方塊。 如果選取處理常式的核取方塊，就會通知處理常式。 如果未選取此核取方塊，則不會通知處理常式。

## <a name="implementing-a-notification-handler"></a>執行通知處理常式

通知處理常式是實作為同進程伺服器的 COM 物件。 通知處理常式必須執行 [**IDsAdminNotifyHandler**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) 介面。

當發生會導致通知的事件時，[使用者和電腦] 嵌入式管理單元會列舉已註冊的通知處理常式，並使用處理程式的 CLSID 來建立每一個通知處理常式。 建立處理常式之後，嵌入式管理單元會呼叫 [**IDsAdminNotifyHandler：： Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) 方法。 **Initialize** 方法會提供嵌入式管理單元與處理常式應接收的事件。

如果事件是應該傳送給通知處理常式的事件，此嵌入式管理單元會呼叫 [**IDsAdminNotifyHandler：： Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) 方法。 **Begin** 方法會提供事件發生時的處理常式、發生事件之物件的相關資料，以及物件將變成的資料（視事件而定）。 **Begin** 方法也會提供嵌入式管理單元，其中包含應該在確認對話方塊中顯示的處理常式文字。

呼叫每個處理常式的 [**Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) 方法時，嵌入式管理單元會顯示確認對話方塊。 確認對話方塊會提示使用者選取要接收通知的處理常式。 如果使用者在確認對話方塊中按下 [ **否** ] 按鈕，系統就不會通知任何處理程式。 如果使用者按下 [ **是]** 按鈕，在 [確認] 對話方塊中選取的每個處理常式都會收到通知。 此嵌入式管理單元會藉由呼叫 [**IDsAdminNotifyHandler：： Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) 方法，將通知傳送給處理常式。

通知所有處理常式之後，嵌入式管理單元會呼叫 [**IDsAdminNotifyHandler：： End**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) 方法。 一律會呼叫 **End** 方法，即使沒有呼叫 [**Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) 方法也一樣。

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>在 Windows 登錄中註冊通知處理常式

和所有 COM 伺服器一樣，必須在 Windows 登錄中註冊通知處理常式。 此處理程式會在下列機碼下註冊：


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**&lt; Clsid &gt;** 是 [**STRINGFROMCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)函數所產生之 clsid 的字串表示。 在 **&lt; &gt; CLSID** 機碼下，有一個 **InProcServer32** 機碼會將物件識別為32位的內部進程伺服器。 在 **InProcServer32** 索引鍵下，DLL 的位置會指定為預設值，而執行緒模型則是在 **>threadingmodel** 值中指定。 所有通知處理常式都必須使用 **單元** 執行緒模型。

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>向 Active Directory 伺服器註冊通知處理常式

在 Active Directory Domain Services 中，通知處理常式註冊是一種地區設定特有的。 如果通知處理常式套用至所有地區設定，則必須在 DisplaySpecifiers 容器中所有地區設定子容器的 **displaySpecifier** 物件中註冊該處理常式。 如果通知處理常式已針對特定地區設定進行當地語系化，則會在該地區設定的 subcontainer 中，將它註冊在 **displaySpecifier** 物件中。 如需 DisplaySpecifiers 容器和地區設定的詳細資訊，請參閱 [顯示](display-specifiers.md) 規範和 [DisplaySpecifiers 容器](displayspecifiers-container.md)。

通知處理常式會在 dsUIAdminNotification 屬性的屬性下註冊至 **DS-UI-預設設定** 容器中。 此為多重值的 Unicode 字串值，其中每個值都需要下列格式：


```C++
<order number>,<CLSID>
```



「 &lt; 訂單編號」 &gt; 是一個不帶正負號的數位，表示處理常式在確認對話方塊中的位置。 當 [確認] 對話方塊出現時，會使用每個值的「訂單編號」比較來排序這些值 &lt; &gt; 。 如果有一個以上的值具有相同的「 &lt; 訂單編號」 &gt; ，這些處理常式會依照從 Active Directory 伺服器讀取的順序來顯示。 非現有的（也就是屬性中的其他值未使用的值）， &lt; &gt; 如果可能的話，應該使用「訂單編號」。 沒有指定的開始位置，而間距可以出現在「 &lt; 訂單編號」 &gt; 序列中。

" &lt; Clsid &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 CLSID 的字串表示。

 

 
