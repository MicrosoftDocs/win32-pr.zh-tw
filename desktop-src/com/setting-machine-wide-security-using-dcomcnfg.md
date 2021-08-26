---
title: 使用 DCOMCNFG 設定 System-Wide 安全性
description: 當您想讓一部電腦上的所有應用程式都未提供自己的安全性以共用相同的預設安全性設定時，您會以全系統為基礎來設定安全性。
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7914fd3b1561900426e2928a5277cb845918e3b8d1b1ad1569ea8db0d112e218
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954368"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>使用 DCOMCNFG 設定 System-Wide 安全性

變更全系統安全性設定會影響所有未設定整個進程安全性的 COM 伺服器應用程式。 這可能會導致這類應用程式無法正常運作。 如果您要變更全系統安全性設定，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。 如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。

當您想讓一部電腦上的所有應用程式都未提供自己的安全性以共用相同的預設安全性設定時，您會以全系統為基礎來設定安全性。 使用 Dcomcnfg.exe 可讓您輕鬆地在登錄中設定適用于電腦上所有應用程式的預設值。

請務必瞭解，如果用戶端或伺服器明確呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定整個進程的安全性，則會忽略登錄中的預設設定，而會使用 **CoInitializeSecurity** 的參數，而不是處理常式的安全性設定。 此外，如果您使用 Dcomcnfg.exe 指定特定進程的安全性設定，則會由處理常式的設定覆寫預設的電腦設定。

啟用全系統安全性時，您必須將驗證等級設定為 [無] 以外的值，而且您必須設定 [啟動] 和 [存取權限]。 您可以選擇設定預設模擬等級，也可以啟用參考追蹤。 下列主題提供逐步程式：

-   [設定 System-Wide 預設驗證層級](#setting-system-wide-default-authentication-level)
-   [設定 System-Wide 啟動許可權](#setting-system-wide-launch-permissions)
-   [設定 System-Wide 存取權限](#setting-system-wide-access-permissions)
-   [設定 System-Wide 模擬等級](#setting-system-wide-impersonation-level)
-   [設定 System-Wide 參考追蹤](#setting-system-wide-reference-tracking)
-   [啟用和停用 DCOM](#enabling-and-disabling-dcom)
-   [相關主題](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>設定 System-Wide 預設驗證層級

驗證層級可用來告知 COM 您希望用戶端進行驗證的層級。 這些層級提供各種保護層級，而不是完整加密的保護。 若要啟用電腦的安全性，您必須選擇 [無] 以外的驗證等級。 您可以藉由完成下列步驟，使用 Dcomcnfg.exe 來選擇這類設定。

**若要以全系統為基礎設定驗證層級**

1.  執行 Dcomcnfg.exe。

2.  選擇 [ **預設** 內容] 索引標籤。

3.  從 [ **DefaultÂ AuthenticationÂ層級** ] 清單方塊中，選擇 [ **無 (])** 以外的值。

4.  如果您要為電腦設定更多屬性，請 **按一下 [套用** ] 按鈕以套用新的驗證層級。 否則，請按一下 **[確定]** 以套用變更並結束 Dcomcnfg.exe。

## <a name="setting-system-wide-launch-permissions"></a>設定 System-Wide 啟動許可權

您使用 Dcomcnfg.exe 設定的啟動許可權會決定使用者清單，其中每個使用者都被明確授與或拒絕啟動任何未提供其本身啟動許可權設定之伺服器的許可權。 設定啟動許可權時，您可以在此清單中新增或移除一或多個使用者或群組。 針對您新增的每個使用者，您必須指定是否要授與或拒絕使用者啟動許可權。

**設定電腦的啟動許可權**

1.  在 Dcomcnfg.exe 的 [**預設安全性**] 屬性頁上，選擇 [**預設啟動許可權**] 區域中的 [**編輯預設值**] 按鈕。

2.  若要移除使用者或群組，請選取您要移除的使用者或群組，然後選擇 [ **移除** ] 按鈕。 選取的使用者或群組將不會再出現在清單方塊中。 當您完成移除使用者和群組時，請選擇 **[確定]**。

3.  如果您想要新增使用者或群組，請選擇 [ **加入** ] 按鈕。

4.  如果您知道想要新增的完整使用者名稱，請在 [ **加入名稱** ] 文字方塊中輸入。 如果您不知道使用者名稱，請參閱 **使用 DCOMCNFG 設定 Processwide 安全性** 來尋找它。 當您找到使用者名稱時，請從 [ **名稱** ] 清單方塊中選取使用者或群組，然後選擇 [ **加入** ] 按鈕。

5.  在 [ **存取類型** ] 清單方塊中，選取 [ **允許啟動** 或 **拒絕啟動**)  (的存取類型。 若要新增其他也會有所選存取類型的使用者，請重複步驟4。 當您完成新增所選存取類型的使用者時，請選擇 [ **確定]** 按鈕。

6.  若要加入將擁有不同類型存取權的使用者，請重複步驟4和5。 否則，請選擇 **[確定]** 以套用變更。

## <a name="setting-system-wide-access-permissions"></a>設定 System-Wide 存取權限

Dcomcnfg.exe 可讓您設定存取權限，以控制被授與或拒絕存取這些伺服器之方法的使用者清單，這些伺服器不提供自己的存取權限。 您可以將使用者或群組新增至清單，以指定是否要授與或拒絕存取權限。 您也可以從清單中移除使用者。

設定存取權限時，您必須確定系統已包含在被授與存取權的使用者清單中。 如果您已將存取權限授與所有人，系統會隱含地包含。

設定電腦存取權限的程式與設定啟動許可權類似。 應採取下列步驟。

**設定電腦的存取權限**

1.  在 Dcomcnfg.exe 的 [**預設安全性**] 屬性頁上，選擇 [**預設存取權限**] 區域中的 [**編輯預設值**] 按鈕。

2.  若要移除使用者或群組，請選取您要移除的使用者或群組，然後選擇 [ **移除** ] 按鈕。 選取的使用者或群組將不會再出現在清單方塊中。 當您完成移除使用者和群組時，請選擇 **[確定]**。

3.  如果您想要新增使用者或群組，請選擇 [ **加入** ] 按鈕。

4.  如果您知道想要新增的完整使用者名稱，請在 [ **加入名稱** ] 文字方塊中輸入。 如果您不知道使用者名稱，請參閱 [使用 DCOMCNFG 設定整個進程的安全性](setting-processwide-security-using-dcomcnfg.md) 來尋找它。 當您找到使用者名稱時，請從 [ **名稱** ] 清單方塊中選取使用者或群組，然後選擇 [ **加入** ] 按鈕。

5.  在 [ **存取類型** ] 清單方塊中，選取 [ **允許存取** ] 或 [ **拒絕存取** ])  (存取類型。 若要加入將擁有所選存取類型的其他使用者，請重複步驟4。 當您完成新增所選存取類型的使用者時，請選擇 [ **確定]** 按鈕。

6.  若要加入將擁有不同類型存取權的使用者，請重複步驟4和5。 否則，請選擇 **[確定]** 以套用變更。

## <a name="setting-system-wide-impersonation-level"></a>設定 System-Wide 模擬等級

用戶端所設定的模擬層級會決定授與給伺服器以代表用戶端的授權數量。 例如，當用戶端將模擬層級設定為委派時，伺服器可以存取本機和遠端資源做為用戶端，而且如果設定了隱匿功能，伺服器可以在多部電腦界限上進行掩蔽。 若要協助判斷您應該選擇哪一種模擬等級，請參閱模擬 [層](impersonation-levels.md) 級和 [掩蓋](cloaking.md)。

設定整部電腦的預設模擬等級，會告知 COM 在電腦上的特定用戶端未使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 或 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)以程式設計方式指定模擬等級時要使用的模擬層級。

**設定電腦的模擬等級**

1.  當 Dcomcnfg.exe 執行時，請選擇 [ **預設屬性** ] 索引標籤。

2.  從 [ **預設模擬等級** ] 清單方塊中，選擇您想要的模擬等級。

3.  如果您要為電腦設定更多屬性，請選擇 [套用 **] 按鈕以** 套用新的模擬等級。 否則，請選擇 **[確定]** 以套用變更並結束 Dcomcnfg.exe。

## <a name="setting-system-wide-reference-tracking"></a>設定 System-Wide 參考追蹤

當您啟用參考追蹤時，會要求 COM 進行額外的安全性檢查，並追蹤會讓物件不會提早釋放的資訊。 請記住，這些額外的檢查很昂貴。 如需參考追蹤的詳細資訊，請參閱 [參考追蹤](reference-tracking.md)。 使用下列步驟來啟用或停用參考追蹤。

**設定電腦的參考追蹤**

1.  當 Dcomcnfg.exe 執行時，請選擇 [ **預設屬性** ] 索引標籤。

2.  若要啟用 (或停用) 參考追蹤，請選取 [ (] 或 [清除]，) 頁面底部附近的 [為 **參考追蹤提供額外的安全性** ] 核取方塊。

3.  如果您要為電腦設定更多屬性，請選擇 [套用 **] 按鈕以** 套用新的設定。 否則，請選擇 **[確定]** 以套用變更並結束 Dcomcnfg.exe。

## <a name="enabling-and-disabling-dcom"></a>啟用和停用 DCOM

當電腦是網路的一部分時，DCOM 有線通訊協定可讓該電腦上的 COM 物件與其他電腦上的 COM 物件進行通訊。 您可以停用特定電腦的 DCOM，但是這樣做會停用該電腦上物件與其他電腦上物件之間的所有通訊。

停用電腦上的 DCOM 不會影響本機 COM 物件。 COM 仍會尋找您已指定的啟動許可權。 如果未指定任何啟動許可權，則會使用預設啟動許可權。 即使您停用 DCOM，如果使用者具有電腦的實體存取權，他們就可以在電腦上啟動伺服器，除非您將啟動許可權設定為不允許。

> [!Note]  
> 如果您停用遠端電腦上的 DCOM，則在重新啟用 DCOM 之後，您將無法從遠端存取該電腦。 若要重新啟用 DCOM，您將需要該電腦的實體存取權。

 

**手動啟用 (或停用電腦的) DCOM**

1.  執行 Dcomcnfg.exe。

2.  選擇 [ **DefaultÂ屬性** ] 索引標籤。

3.  選取 (或清除 [ **在這部電腦上啟用分散式 COMÂ** ] 核取方塊) 。

4.  如果您要為電腦設定更多屬性，請 **按一下 [套用** ] 按鈕來啟用 (或停用) DCOM。 否則，請按一下 **[確定]** 以套用變更並結束 Dcomcnfg.exe。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定整個進程的安全性](setting-processwide-security.md)
</dt> </dl>

 

 




