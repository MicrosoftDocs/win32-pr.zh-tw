---
description: 有時您可能需要在執行中的系統上安裝較新版本的提供者。
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: 更新提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8c40a3d50672115478ae62135774f5a1aad93373bd5b844402e89462b44fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757648"
---
# <a name="updating-a-provider"></a>更新提供者

有時您可能需要在執行中的系統上安裝較新版本的提供者。 如果您的提供者是安裝成 DLL，您可以安裝新的提供者，而不需要重新開機服務、重新開機電腦，或在當時使用 WMI 影響任何應用程式。

下列程式說明如何更新提供者。

**更新提供者**

1.  建立新的提供者。

    1.  使用不同的 DLL 名稱和不同的 **CLSID** 來編譯新的提供者。

        例如，將 Myprov.dll 變更為 Myprov1.dll，並將 **clsid \_ MyProProv** 變更為 **clsid \_ MyProv** 1。

    2.  修改提供者註冊 MOF 檔案，以使用新的 CLSID (CLSID \_ MyProv1) ，但 ( "MyProv" ) 相同的提供者名稱。

2.  安裝新的提供者。

    1.  將新的提供者 DLL 連同舊的名稱一起複製。
    2.  自行註冊新的提供者。

        例如，使用 **regsvr32** **myprov1.dll** 命令來註冊新的提供者。

    3.  編譯新的提供者註冊 MOF，進而覆寫舊的提供者註冊。 到目前為止，舊的提供者完全正常運作;新的提供者現在已可完全運作。

3.  如有必要，請移除舊版本的提供者。

    1.  取消註冊舊的 DLL。

        例如，使用 **regsvr32** **/umyprov.dll** 命令取消註冊舊的 DLL。

    2.  藉由呼叫 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa)，標記要在重新開機時刪除的舊 DLL。

您可以採取類似的步驟來升級本機伺服器執行的提供者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> </dl>

 

 
