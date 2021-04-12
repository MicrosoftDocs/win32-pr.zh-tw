---
title: 簡化遊戲安裝
description: 本文概述 Windows 遊戲開發人員可以和執行的一些概念，以改善整體體驗。
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8728eb2c9c53a99673ee742a5c961b91e37abed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315853"
---
# <a name="simplifying-game-installation"></a>簡化遊戲安裝

在主控台而不是在 Windows 上執行之遊戲的主要優點之一，就是安裝程式或缺乏。 當遊戲首次在主控台上執行時，播放程式會進行一些選擇或確認，而且幾乎可以立即開始播放。 相較之下，在 Windows 上安裝遊戲比較複雜，因為它需要大量的使用者輸入，以及可能會有很長的安裝流程。 不過，您可以改進此安裝程式，以提供更好的 Windows 遊戲玩家體驗。 本文概述 Windows 遊戲開發人員可以和執行的一些概念，以改善整體體驗。

-   [一般遊戲安裝](#typical-game-installation)
-   [簡化的遊戲安裝](#simplified-game-installation)
    -   [事先詢問所有問題](#ask-all-questions-up-front)
    -   [提供特殊的安裝模式](#provide-special-installation-modes)
    -   [將安裝問題的數量降到最低](#minimize-the-quantity-of-installation-questions)
    -   [將選用元件變更為必要元件](#change-optional-components-into-required-components)
    -   [一律安裝 DirectX，然後以無訊息模式進行](#always-install-directx-and-do-so-silently)
    -   [思考您的 EULA](#think-about-your-eula)
    -   [在安裝後自動啟動](#automatically-launch-after-installation)
    -   [優化您的安裝效能](#optimize-your-installation-performance)
    -   [在安裝期間註冊 Windows 防火牆](#register-with-windows-firewall-during-installation)
    -   [為所有使用者安裝，而不只是目前的使用者](#install-for-all-users-not-just-the-current-user)
-   [簡化安裝的範例](#example-of-simplified-installation)
-   [總結](#summary)

## <a name="typical-game-installation"></a>一般遊戲安裝

比較輕鬆安裝和開始玩遊戲所需的時間量時，一般的 Xbox 體驗優於 Windows。 圖1中的流程圖顯示 Xbox 和 Windows 上的一般安裝程式，以進行比較。

**圖1。一般安裝程式，Xbox 與 Windows**

![xbox \- 與 \- pc](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>簡化的遊戲安裝

但是，使用者在 Windows 上安裝遊戲的需求愈大，就不需要。 藉由執行下列概念，您將會減少使用者必須完成的步驟數目，這可以縮短安裝所需的時間量。

### <a name="ask-all-questions-up-front"></a>事先詢問所有問題

玩家在安裝期間選取的所有選擇（可能會導致安裝中止），都應該在不停止安裝的選項之前提供;最糟的情況是讓玩家能夠選擇是否要在遊戲完全從安裝媒體複製之後，才會中止安裝。 如果安裝需要交換多個磁片才能完成，則這可能會很令人沮喪。 您應該設計您的安裝程式來要求所有重要的問題 (例如，在程式開始時接受 EULA) ，如此就不需要在完成時回復或完成安裝。

當遊戲初次開機時，您也可以提示使用者接受 EULA，並輸入產品金鑰，而不是在安裝過程中要求這些金鑰。 在此案例中，拒絕接受 EULA 或在產品金鑰輸入期間取消，將不會回復安裝，因為這些提示是遊戲本身的一部分。 如果您已經預先安裝或 OEM 案例，這可能會很有用。 不過，請注意，不要在初始啟動時提示使用者進行需要系統管理認證的選擇。

### <a name="provide-special-installation-modes"></a>提供特殊的安裝模式

在理想的情況下，Windows 遊戲安裝程式應該只提供完全自動和自訂的安裝模式，以及兩者之間的任何內容。

自動模式不應詢問任何其他問題，而不是建立正常運作的安裝所需的任何問題，而且只使用預設設定，而不提示其他選項。 很多玩家都不在意遊戲在硬碟上的位置，也不在意最初的遊戲設定，只是想要儘快玩遊戲。

自訂模式應僅適用于需要或想要變更安裝路徑或其他安裝選項，而且不應該是預設模式的 power 使用者。

自訂模式可以提供完整安裝或最小安裝的選擇，只安裝播放遊戲所需的檔案。 如果玩家選擇的是安裝的最小值，則遊戲可以使用隨選安裝或串流處理技術來讀取剩餘的安裝資料，讓玩家可以快速開始播放遊戲，而不需要等待完整安裝完成。 不過，以這種方式安裝資料會影響遊戲引擎的設計。 如需有關隨選安裝內容的詳細資訊，請參閱 [遊戲的隨選安裝](/windows/desktop/DxTechArts/install-on-demand-for-games)。

### <a name="minimize-the-quantity-of-installation-questions"></a>將安裝問題的數量降到最低

在這兩個安裝模式中，您應該嘗試限制安裝期間提示玩家的次數。 這樣可減少安裝和執行遊戲所需的讀取量。 必要時，在安裝完成之後，應該只會出現一個後續的提示。 如您所見，[圖 1] 所示的範例中有太多安裝後提示。

### <a name="change-optional-components-into-required-components"></a>將選用元件變更為必要元件

除非有很好的理由，否則請安裝所有必要元件，而不是將它們設為選用。 只要安裝所有的元件，就會啟動遊戲，而不會有進一步的延遲和條理。

### <a name="always-install-directx-and-do-so-silently"></a>一律安裝 DirectX，然後以無訊息模式進行

強烈建議遊戲以無訊息模式安裝遊戲所用的 DirectX 可轉散發套件。 DirectX 安裝程式的設計目的，是要驗證是否需要更新任何事項，並在不需要時快速傳回。 因此，如果使用者想要安裝 DirectX，就不需要詢問使用者。 您可以從安裝套件執行此命令來完成 DirectX 的無訊息安裝： **dxsetup.exe/silent**

詢問使用者是否要安裝 DirectX 可能會造成許多問題。 例如，如果使用者假設他已安裝最新的可轉散發套件，並選擇略過 DirectX 的安裝;遊戲的安裝仍可順利執行。 但是，如果遊戲需要特定版本的 D3DX 或其他已略過的已更新功能，則遊戲將無法運作，而且使用者將會感到非常挫折。

如果基於某些原因，您必須詢問使用者是否要安裝 DirectX，如果使用者選擇不安裝 DirectX，則您的安裝程式至少應該中止並回復整個安裝程式。 復原安裝將可避免系統在遊戲啟動時未安裝最新版本的 DirectX 所造成的任何錯誤。

請注意，請務必寄送您的遊戲所用的可轉散發套件，而不只是從最新的 DirectX SDK 寄送可轉散發套件。 最新的可轉散發套件可能不包含在先前版本中找到的所有元件。

也請務必讓安裝程式檢查以查看已安裝的內容，並判斷是否需要重新開機系統。 如果 DirectX 是最新的，則複製一個 DLL 不應該需要重新開機。

### <a name="think-about-your-eula"></a>思考您的 EULA

DirectX EULA 可以和應該附加至遊戲開發人員的授權合約。 不允許使用者同意開發人員的授權合約，而不是 DirectX EULA。 使用者必須同意 Eula 或不安裝遊戲。 如果開發人員覺得她必須為使用者提供選擇，則如果使用者選擇不同意 DirectX EULA，則整個安裝應該會失敗。

可能的話，請洽詢您的法律部門，看看您是否可以完全避免 Eula，並使用像是主控台遊戲使用的壓縮包裝式 EULA。 這可避免在使用者想要接受 EULA 時要求他們。 DirectX EULA 必須附加至壓縮包裝的授權合約;否則，就必須顯示和接受 DirectX EULA，以因應使用壓縮包裝的授權合約的目的。

壓縮包裝的授權合約有一個例外，是針對內容編輯器。 任何編輯器都需要在編輯器安裝期間顯示 EULA，或在第一次啟動編輯器時顯示 EULA。 許多玩家都只有興趣播放而不是進行內容，因此安裝編輯器應該是個別的進程。

### <a name="automatically-launch-after-installation"></a>在安裝後自動啟動

幾乎所有玩家都希望在收到遊戲時立即播放遊戲。 根據預設，安裝程式應在完成安裝之後啟動遊戲，雖然在自訂安裝中是很好的作法，但是在使用者可能會覆寫的核取方塊中指定此選項。

### <a name="optimize-your-installation-performance"></a>優化您的安裝效能

開發人員應該測試其安裝，以判斷安裝需要多少時間。 開發人員可以使用其安裝工具的最新版本，以及藉由將安裝媒體上的資料版面配置優化，來縮短安裝時間。 大部分的 DVD 製作工具都具有版面配置優化的選項，可改善安裝時間，而不會增加開發工作負載。

### <a name="register-with-windows-firewall-during-installation"></a>在安裝期間註冊 Windows 防火牆

如果您的遊戲可作為伺服器執行，或遊戲網路模型是對等，請在安裝時向 Windows 防火牆註冊您的遊戲。 這可防止在使用者嘗試存取網路時，防火牆對話方塊出現在遊戲中間。 如果遊戲是單純的用戶端，則安裝程式不應將遊戲新增至防火牆的例外清單。

如需詳細資訊，請參閱適用于遊戲開發人員的 Windows 防火牆。

### <a name="install-for-all-users-not-just-the-current-user"></a>為所有使用者安裝，而不只是目前的使用者

預設是為所有使用者安裝遊戲。 如此一來，系統上的任何新使用者都可以播放遊戲，而不需要為他們安裝。 如果嘗試在 Least-Privileged 使用者帳戶上安裝所有使用者，安裝程式將會失敗，或提示使用者輸入系統管理員密碼。 因此，在提供為所有使用者安裝選項之前，請先嘗試偵測帳戶是否具有適當的許可權。 如果使用者選擇只為目前的使用者安裝遊戲，請務必將安裝路徑變更為使用者設定檔中的位置。 在理想的情況下，請將路徑變更為非漫遊應用程式資料中的某處 (例如，CSIDL \_ LOCAL \_ APPDATA) 的子目錄。

## <a name="example-of-simplified-installation"></a>簡化安裝的範例

在 [圖 2] 中，您可以利用簡化的安裝對話方塊，以改良的方式在 Windows 中安裝遊戲的流程範例。

**[圖 2]簡化的安裝流程**

![安裝](images/simplifiedgameinstall.png)

以下是重要的注意事項：

-   插入安裝光碟 (自動執行) 時，會自動啟動安裝程式。
-   如果電腦尚未安裝此遊戲，則不會顯示啟動顯示畫面（具有安裝、移除、查看網站或結束的選項）。
-   **安裝** 對話方塊是安裝程式所顯示的第一個對話方塊。
-   [ **安裝** ] 按鈕是自動安裝模式的執行。
-   [ **選項** ] 按鈕是自訂安裝模式的執行。
-   [ **取消** ] 按鈕會立即結束安裝程式。 因為啟動安裝程式對使用者來說是一個簡單的動作，所以不會提示確認。
-   一旦使用者接受 EULA 並輸入有效的產品金鑰，就會開始安裝。
-   當安裝程式完成時，遊戲將會自動啟動，或顯示一個對話方塊來通知使用者安裝已完成，並根據是否選取 [ **在安裝後執行遊戲** ] 來提供任何其他選項。
-   為了方便起見，[ **執行遊戲** ] 核取方塊提供另一次啟動遊戲的機會。 此選項一律預設為未選取，因為只有在安裝 [**安裝選項**] 對話方塊中取消選取 [安裝完成] 對話方塊 **之後**，才會顯示 [**安裝完成**] 對話方塊。
-   [ **確定]** 按鈕會關閉對話方塊，並選擇性地在 **執行** 時採取動作並 **查看讀我檔案** 核取方塊。

## <a name="summary"></a>總結

玩家希望儘快播放遊戲。 玩家想要做的最後一件事，就是透過對話來費力，然後選擇與他或她已安裝的所有其他遊戲一樣。 執行這些構想可以縮短玩家花在 Windows 上安裝遊戲的時間，並協助改善 Windows 遊戲體驗的整體品質。

 

 