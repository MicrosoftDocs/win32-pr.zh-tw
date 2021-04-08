---
title: 認證您的桌面應用程式
description: 請遵循下列步驟，讓您的桌面應用程式通過 Windows 7、Windows 8、Windows 8.1 和 Windows 10 的認證。如果您想要轉換您的傳統型應用程式，使其與通用 Windows 平臺和 Windows Store 相容，您將使用 Windows 傳統型橋接器，在這種情況下，您應該遵循認證步驟的傳統型橋接器指導方針。如果您要從一開始就開發和驗證 UWP 應用程式，請參閱 UWP 中的 Windows 應用程式認證指引以取得認證資訊。
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684172"
---
# <a name="certify-your-desktop-application"></a>認證您的桌面應用程式

> [!IMPORTANT]
> Win32 桌面應用程式的憑證已 [淘汰](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920)。 相反地，請 [在此提交檔](https://www.microsoft.com/wdsi/filesubmission/)。

請遵循下列步驟，讓您的桌面應用程式通過 Windows 7、Windows 8、Windows 8.1 和 Windows 10 的認證。

如果您想要轉換您的傳統型應用程式，使其與通用 Windows 平臺和 Windows Store 相容，您將使用 [Windows 傳統型橋接器](https://developer.microsoft.com/windows/bridges/desktop)，在這種情況下，您應該遵循認證步驟的 [傳統型橋接器](/windows/uwp/porting/desktop-to-uwp-root) 指導方針。

如果您要從一開始就開發和驗證 UWP 應用程式，請參閱 [UWP 中的 Windows 應用程式認證指引](/windows/uwp/debug-test-perf/windows-app-certification-kit) 以取得認證資訊。

## <a name="step-1-prepare-for-certification"></a>步驟1：準備認證



| 主題                                                                                       | 描述                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [有哪些優點？](what-are-the-benefits-.md)<br/>                             | 認證您的桌面應用程式可為您和您的客戶提供數個優點。              |
| [閱讀需求](certification-requirements-for-windows-desktop-apps.md)<br/> | 查看傳統型應用程式必須滿足的技術需求和資格資格。 |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a>步驟2：使用 Windows 應用程式認證套件測試您的應用程式



| 主題                                                          | 描述                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [取得套件](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | 若要認證您的應用程式，您必須安裝並執行 Windows SDK) 中包含的 Windows 應用程式認證套件 (。                                                                     |
| [使用套件](using-the-windows-app-certification-kit.md)   | 在您可以提交應用程式之前，您必須先測試應用程式是否就緒。 您也可以下載一份 [應用程式認證白皮書](https://www.microsoft.com/download/details.aspx?id=27414)。 |
| [審核測試詳細資料](windows-app-certification-kit-tests.md) | 取得您的應用程式必須傳遞的測試清單，以符合最新 Windows 作業系統的相容性。                                                               |



 

注意：篩選器驅動程式也必須通過 [硬體認證套件](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe)。  (參閱 [Windows 傳統型應用程式的認證需求，第6.2 節](certification-requirements-for-windows-desktop-apps.md)。 ) 

## <a name="step-3-use-the-windows-certification-dashboard"></a>步驟3：使用 Windows 認證儀表板

若要提交認證的應用程式，您必須在 [Windows 認證儀表板](/previous-versions/hh833792(v=msdn.10))上登入或註冊公司帳戶。 一旦您這樣做，不僅能讓您的應用程式通過認證，還可以存取工具，在程式的所有階段檢查及管理您的應用程式。



| 主題                                                                                                                   | 描述                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [設定帳戶](/windows-hardware/drivers/dashboard/)                 | 如果您的公司尚未註冊，您必須透過 Windows 認證儀表板註冊。                                        |
| [取得程式碼簽署憑證](/windows-hardware/drivers/dashboard/)      | 建立 Windows 認證儀表板帳戶之前，您必須先取得程式碼簽署憑證來保護您的數位資訊。 |
| [在本機測試並上傳結果](/windows-hardware/drivers/dashboard/) | 在您執行 Windows 應用程式認證套件測試之後，請將結果上傳至 Windows 認證儀表板。                                 |
| [管理您的提交內容](/windows-hardware/drivers/dashboard/)              | 提交您的應用程式以進行認證之後，您可以透過 Windows 認證儀表板審查您的提交內容。                           |



 

## <a name="step-4-promote-your-desktop-app"></a>步驟4：升級您的桌面應用程式



| 主題                                                                      | 描述                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [檢查應用程式相容性](/windows/compatibility/windows-8-1-introduction) | 如果您正在建立 Windows 8.1 的應用程式，請調查相容性問題。                                           |
| [搭配您的應用程式使用標誌](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | 根據指導方針，顯示封裝和廣告中的標誌，以及其他促銷材料。 僅適用于 Windows 7。 |



 

## <a name="see-also"></a>另請參閱：

[應用程式相容性論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility)：從社區尋找相容性與標誌認證的支援。

[Windows SDK 的 blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/)：尋找與應用程式認證相關的秘訣和新聞。

[Windows Server 論壇]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat)：造訪認證論壇以取得解答。

[相容性操作手冊](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)：取得最新 Windows 版本的新功能或變更的相關資訊。

 

