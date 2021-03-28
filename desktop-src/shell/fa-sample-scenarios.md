---
description: 在下列範例中，假設軟體發展公司稱為 Litware，Inc.。
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: 檔案關聯範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111752"
---
# <a name="file-association-example"></a>檔案關聯範例

在下列範例中，名為 Litware，Inc. 的假想軟體發展公司會建立名為 LitwarePlayer 的新音訊播放機。 Litware 想要設計 LitwarePlayer 與其主要檔案類型之間的檔案關聯，其使用新開發的音訊格式，可讓整個音訊 CD 儲存在 10 kb 以內的記憶體中，且不會失去品質。

> [!IMPORTANT]
> 本主題不適用於 Windows 10。 預設檔案關聯在 Windows 10 中的運作方式有所變更。 如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。

 

## <a name="designing-a-new-file-association"></a>設計新的檔案關聯

公司應採取下列步驟。

1.  **決定是否應將新的檔案類型視為公用或私用。** 這個新的檔案類型是媒體類型。 由於使用者會跨各種平臺交換媒體檔案，而且可能會有其他需要讀取 LitwarePlayer 格式的應用程式，因此， [公用](fa-file-types.md) 檔案類型是最適當的。
2.  **判斷是否已定義此檔案類型。** 檢查網際網路指派的號碼授權單位 (IANA) MIME 資料庫，以及網際網路上的其他公用檔案類型資料庫，判斷沒有定義任何可比較的檔案類型。 因為這是新的檔案格式，所以您需要定義新的檔案類型。
3.  **定義新檔案類型的副檔名。** 開發人員會選擇 `.opa-ltw-audio` ，其中包含其廠商縮寫，以及檔案所包含內容的提示。 研究判斷此延伸模組未由其他人使用。 遵循目前的建議，未定義任何簡短的延伸模組。
4.  **為檔案類型定義 MIME 類型，並向 IANA 註冊。** Litware 會將新的 MIME 類型定義為 *音訊/LitwarePlayer* ，並準備 MIME 類型應用程式，並遵循 (RFC) 號碼2045、2046、2047和2048提出的指導方針。 然後，他們會將應用程式提交至 IANA，以將新的檔案類型新增至已註冊之 MIME 類型的資料庫。
5.  **判斷檔案類型是否存在 ProgID。** 因為這是新的檔案類型，所以不會有 [ProgID](fa-progids.md) 。 針對 LitwarePlayer 設計新 ProgID 的 Litware 集。 他們會決定易記名稱 "LitwarePlayer Audio Player" (儲存為 LitwarePlayer.exe 檔案) 中的資源，並針對與 LitwarePlayer 相關聯的檔案設計要使用的預設圖示 (也儲存在 LitwarePlayer.exe) 中。 因為 LitwarePlayer 是新的應用程式，所以這是第1版的 ProgID。
6.  **註冊 ProgID。** 安裝 LitwarePlayer 時，安裝程式會在登錄中建立下列 [ProgID](fa-progids.md) 專案。

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    在命令索引鍵中，會將 %1 傳遞為要播放之檔案的路徑。

7.  **註冊檔案類型的副檔名。** 當安裝 LitwarePlayer 時，安裝程式會在登錄中為其自訂檔案類型延伸建立下列專案。

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> 每當建立或變更檔案關聯時，就會藉由呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)來指定 SHCNE ASSOCCHANGED 事件，以通知系統已進行變更 \_ 。 如果未這麼做，Shell 可能無法辨識在系統重新開機之前所做的任何變更。

 

## <a name="additional-resources"></a>其他資源

-   [檔案關聯簡介](fa-intro.md)
-   [如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)
-   [將應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案關聯的最佳作法](fa-best-practices.md)
</dt> <dt>

[在 Windows Vista 和更新版本中管理預設應用程式的指導方針](vista-managing-defaults.md)
</dt> <dt>

[預設程式](default-programs.md)
</dt> <dt>

[ (SPAD) 設定程式存取和電腦預設值 ](cpl-setprogramaccess.md)
</dt> </dl>

 

 
