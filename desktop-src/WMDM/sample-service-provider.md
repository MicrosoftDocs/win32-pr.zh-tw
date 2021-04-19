---
title: 範例服務提供者
description: 範例服務提供者
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- Windows Media 裝置管理員、服務提供者範例
- 裝置管理員，服務提供者範例
- 服務提供者，範例
- 範例，服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106991287"
---
# <a name="sample-service-provider"></a>範例服務提供者

Windows Media 裝置管理員 SDK 包含可供您使用的範例服務提供者。 此服務提供者包含的類別會報告電腦上的每個硬碟，就像是連接的裝置一樣。 將使用此服務提供者的唯一應用程式是範例應用程式;Windows 檔案總管將不會看到此服務提供者所報告的「裝置」。 服務提供者範例是以 ATL 建立的 COM 物件。 下列步驟說明如何使用範例服務提供者：

> [!Note]  
> 範例服務提供者會執行很少的功能，因此不應該用於測試 Windows Media 裝置管理員應用程式。 若要測試應用程式，請使用完全執行的服務提供者。

 

-   此範例隨附的程式碼錯誤，會導致服務提供者無法正常運作。 若要更正這個錯誤，請開啟安裝在 < *SDK 安裝路徑* WMFSDK95 WMDM mdsp mshdsp 資料夾中的 MDSPEnumStorage .cpp 檔案  > \\ \\ \\ \\ ，移至第185行，然後變更下行：

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

為此值：

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  編譯 MsHDSP.dll 檔案。 您可以使用 NMAKE 或 Visual Studio 來進行這項作業。 請參閱 [使用 NMAKE 編譯範例服務提供者](compiling-the-sample-service-provider-using-nmake.md) 或 [使用 Visual Studio 編譯範例服務提供者](compiling-the-sample-service-provider-using-visual-studio.md) ，以瞭解如何編譯應用程式。
2.  使用 regsvr32 註冊 MsHDSP.dll。 在與 MsHDSP.dll 相同的資料夾中，輸入至命令提示字元視窗的下列程式程式碼，將會註冊範例服務提供者：

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    若要停止模擬裝置，請在命令提示字元中輸入下列程式程式碼：

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  此 DLL 所模擬的卸載式裝置只能由這個 SDK 隨附的範例應用程式查看。 使用 [範例桌面應用程式](sample-desktop-application.md)中所述的其中一種方法來編譯範例應用程式。
4.  若要使用 Visual Studio 來偵測服務提供者，請在 Visual Studio 中開啟服務提供者，然後選取 [**調試** 程式] 功能表上的 [**啟動**]。 在快顯對話方塊中，流覽至您在上一個步驟中建立的範例應用程式，然後按一下 **[確定]**，服務提供者就會開始在 [偵測] 模式下執行。

    若要執行服務提供者，而不在 Visual Studio 中進行偵錯工具，只要註冊 msdhsp.dll，然後執行 SDK 隨附的範例桌面應用程式即可。 範例桌面應用程式會自動執行範例服務提供者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**範例**](samples.md)
</dt> </dl>

 

 




