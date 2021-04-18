---
title: 如何針對應用程式封裝簽章錯誤進行疑難排解
description: 應用程式部署失敗的原因可能是無法驗證應用程式套件的數位簽章。 瞭解如何辨識這些失敗，以及該怎麼做。
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6f50dc5ff428e74f4928fc20775b13de7c3be9
ms.sourcegitcommit: 784b5954a1646e2406cd4ee27a9e4f50e28ee9b7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106976309"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>如何針對應用程式封裝簽章錯誤進行疑難排解

應用程式部署失敗的原因可能是無法驗證應用程式套件的數位簽章。 瞭解如何辨識這些失敗，以及該怎麼做。

當您部署已封裝的 Windows 應用程式時，Windows 一律會嘗試驗證應用程式套件上的數位簽章。 簽章驗證期間的失敗會封鎖封裝的部署。 但是，為什麼封裝未進行驗證可能並不明顯。 尤其是，如果您使用私人憑證簽署套件以進行本機測試，您通常也必須管理這些憑證的信任。 不正確的憑證信任設定可能會導致簽章驗證失敗。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [封裝、部署及查詢 Windows 應用程式](appx-portal.md)
-   [憑證信任驗證](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>必要條件

-   用來診斷安裝失敗的[Windows 事件記錄](/windows/desktop/WES/windows-event-log)檔。
-   [用於](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) 在疑難排解期間管理憑證存放區操作之憑證的 Certutil 工作

## <a name="instructions"></a>指示

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>步驟1：檢查事件記錄檔中的診斷資訊

根據您嘗試部署應用程式的方式而定，您可能並未收到有意義的錯誤碼來部署失敗。 在此情況下，您通常可以直接從事件記錄檔取得錯誤碼。

**若要從事件記錄檔取得錯誤碼**

1.  執行 **eventvwr.msc services.msc**。
2.  移至 **事件檢視器 (本機)**  >  **應用程式和服務記錄**  >  **Microsoft**  >  **Windows**。
3.  第一個要檢查的記錄是 **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**。
4.  部署相關錯誤會記錄在 **appxdeployment-server-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational** 中。

    針對部署錯誤，請搜尋最新的錯誤事件404。 此錯誤事件會為您提供錯誤碼，以及部署失敗原因的說明。 如果錯誤事件465之前是404事件，開啟封裝時發生問題。

如果未發生465錯誤，請參閱一般針對 [封裝、部署及查詢 Windows 應用程式進行疑難排解](troubleshooting.md)。 否則，請參閱此表格，以取得可在錯誤事件465的錯誤字串中顯示的常見錯誤碼：

| 錯誤碼 | 錯誤                                 | 描述                                                                                                          | 建議                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | \_安裝 \_ 開啟 \_ 套件 \_ 失敗 | 無法開啟應用程式封裝。                                                                                 | 此錯誤通常表示套件有問題。 您必須重新建立並簽署封裝。 如需詳細資訊，請參閱 [使用應用程式封裝程式](make-appx-package--makeappx-exe-.md)。 |
| 0x80080205 | APPX \_ E \_ 不正確 \_ BLOCKMAP            | 應用程式套件已遭篡改，或具有不正確區塊對應。                                                  | 封裝已損毀。 您必須重新建立並簽署封裝。 如需詳細資訊，請參閱 [使用應用程式封裝程式](make-appx-package--makeappx-exe-.md)。                                  |
| 0x800B0004 | 信任 \_ 電子 \_ 主體 \_ 不 \_ 受信任       | 應用程式套件已遭修改。                                                                              | 套件內容不再符合其數位簽章。 您必須重新簽署封裝。 如需詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。  |
| 0x800B0100 | 信任 \_ 電子 \_ NOSIGNATURE                 | 應用程式套件未簽署。                                                                                         | 只能部署已簽署的 Windows 應用程式套件。 如需簽署應用程式套件的相關資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。                  |
| 0x800B0109 | CERT \_ E 未 \_ 受信任的 \_ 根              | 用來簽署應用程式套件的憑證鏈會以不受信任的根憑證結尾。           | 繼續進行步驟2以疑難排解憑證信任。                                                                                                                                                  |
| 0x800B010A | CERT \_ E \_ 連結                     | 從用來簽署應用程式套件的憑證中，無法將任何憑證鏈建立至信任的根授權單位。 | 繼續進行步驟2以疑難排解憑證信任。                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>步驟2：判斷用來簽署應用程式套件的憑證鏈

若要找出本機電腦必須信任的憑證，您可以在應用程式套件上檢查憑證鏈中的數位簽章。

**判斷憑證鏈**

1.  在檔案總管中，以滑鼠右鍵按一下應用程式套件，然後選取 [ **屬性**]。
2.  在 [ **屬性** ] 對話方塊中，選取 [ **數位簽章** ] 索引標籤，此索引標籤也會顯示是否可以驗證簽章。
3.  在 [簽章] 清單中選取簽章，然後按一下 [ **詳細資料** ] 按鈕。
4.  在 [ **數位簽章詳細資料** ] 對話方塊中，按一下 [ **視圖憑證** ] 按鈕。
5.  在 [ **憑證** ] 對話方塊中，選取 [ **憑證路徑** ] 索引標籤。

鏈中的最上層憑證是根憑證，而底部的憑證則是簽署憑證。 如果鏈中只有單一憑證，則簽署憑證也是自己的根憑證。 您可以為每個使用 [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))的憑證判斷序號：

**判斷每個憑證的序號**

1.  在 [憑證路徑] 窗格中，選取憑證，然後按一下 [ **View certificate**]。
2.  在 [憑證] 對話方塊中，選取 [ **詳細資料** ] 索引標籤，此索引標籤會顯示憑證的序號和其他有用的屬性。

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>步驟3：判斷本機電腦所信任的憑證

若要能夠部署應用程式套件，它不僅能在使用者的內容中受信任，也不能在本機電腦內容中受到信任。 如此一來，當您在上一個步驟的 [數位簽章] 索引標籤中查看時，數位簽章可能會顯示為有效，但在應用程式套件部署期間仍無法通過驗證。

**判斷用來簽署應用程式套件的憑證鏈是否由本機電腦明確信任**

1.  請執行這個命令：

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  請執行這個命令：

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

如果您未指定憑證序號， [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) 會列出該存放區的本機電腦所信任的所有憑證。

封裝可能會因為憑證鏈錯誤而無法安裝，即使簽署憑證不是自我簽署的憑證，以及根憑證在本機電腦的根存放區中。 在此情況下，可能會有中繼憑證授權單位單位的信任問題。 如需此問題的詳細資訊，請參閱 [使用憑證](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85))。

## <a name="remarks"></a>備註

如果您決定因為簽署憑證不受信任而無法部署封裝，除非您知道它的來源，並信任它，否則請勿安裝套件。

如果您想要以手動方式信任安裝的應用程式 (例如，安裝您自己的測試簽署應用程式套件) ，您可以從應用程式套件手動將憑證新增至本機電腦憑證信任。

**手動將憑證新增至本機電腦憑證信任**

1.  在檔案總管中，以滑鼠右鍵按一下應用程式套件，然後在快顯功能表中選取 [ **屬性**]。
2.  在 [ **屬性** ] 對話方塊中，選取 [ **數位簽章** ] 索引標籤。
3.  在 [簽章] 清單中選取簽章，然後按一下 [ **詳細資料** ] 按鈕。
4.  在 [ **數位簽章詳細資料** ] 對話方塊中，按一下 [ **視圖憑證** ] 按鈕。
5.  在 [**憑證**] 對話方塊中，按一下 [**安裝憑證 ...** ]。 按鈕。
6.  在 [憑證匯入] 嚮導中選取 [ **本機電腦** ]，然後按 **[下一步]**。 您將需要授與系統管理員許可權才能繼續。
7.  選取 **[將所有憑證放入以下的存放區** ]，然後流覽至 [ **受信任的人** ] 存放區。
8.  按 **[下一步**]，然後按一下 **[完成** ] 以完成 wizard。

在此手動新增之後，您可以在 [ **憑證** ] 對話方塊中看到憑證現在是受信任的。

您可以在不再需要憑證之後，將它移除。

**移除憑證**

1.  以系統管理員身分執行 **Cmd.exe** 。
2.  在系統管理員命令提示字元中，執行此命令：

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  尋找您所安裝之憑證的序號。 這個數位是 *certID*。
4.  請執行這個命令：

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

建議您避免手動將根憑證新增至本機電腦的「 [受信任的根憑證授權單位」憑證存放區](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)。 如果有多個應用程式是以連結至相同根憑證的憑證來簽署，例如企業營運應用程式，則會比將個別憑證安裝至受信任的人存放區更有效率。 [受信任的人] 存放區包含預設視為受信任的憑證，因此不會由較高的授權單位或憑證信任清單或鏈進行驗證。 如需將憑證新增至「信任的根憑證授權單位」憑證存放區的考慮，請參閱程式 [代碼簽署最佳做法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))。

## <a name="security-considerations"></a>安全性考量

藉由將認證新增至[本機電腦憑證存放區](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores) (英文)，您會對電腦上所有使用者的憑證信任造成影響。 建議您將任何要用於測試應用程式套件的程式碼簽署憑證，安裝到 [受信任的人] 憑證存放區。 當不再需要時，請立即移除這些憑證，以防止它們被用來危害系統信任。 如果您建立自己的測試憑證來簽署應用程式套件，我們也建議您限制與測試憑證相關聯的許可權。 如需建立測試憑證以簽署應用程式套件的相關資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**範例**
</dt> <dt>

[建立應用程式套件範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**概念**
</dt> <dt>

[對 Windows 應用程式的封裝、部署及查詢進行疑難排解](troubleshooting.md)
</dt> <dt>

[用於管理憑證的 Certutil 工作](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 
