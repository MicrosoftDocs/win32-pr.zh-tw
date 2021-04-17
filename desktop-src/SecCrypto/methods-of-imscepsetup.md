---
description: IMSCEPSetup 介面所定義的方法。
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: IMSCEPSetup 的方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f543bb4525a3335128846ec5724e1a9a09a35f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511816"
---
# <a name="methods-of-imscepsetup"></a>IMSCEPSetup 的方法

下列方法是由 [**IMSCEPSetup**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) 介面所定義。 這裡不會顯示內容存取方法。 若要查看 **IMSCEPSetup** 的屬性，請參閱 [IMSCEPSetup 的屬性](properties-of-imscepsetup.md)。



| 方法                                                             | 描述                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | 取得指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 所支援的 [*金鑰長度*](../secgloss/k-gly.md)清單。 |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | 取得網路裝置註冊服務 (NDES) 設定的屬性值。                                                                                                                                                                                               |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | 取得在電腦上提供非對稱金鑰簽章和 exchange 演算法的 Csp 清單。                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | 使用預設值初始化 **CMSCEPSetup** 物件，以啟用 NDES 角色的安裝。                                                                                                                                                                                  |
| [**安裝**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | 安裝 **CMSCEPSetup** 物件中設定的角色。                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | 一律傳回 **VARIANT \_ TRUE** ，不應該使用。                                                                                                                                                                                                                          |
| [**卸載後**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | 這個方法尚未實作。 保留供以後使用                                                                                                                                                                                                                    |
| [**卸載前**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | 移除 NDES 角色的登錄和 IIS 設定。                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | 設定 IIS NDES 延伸模組所使用的使用者帳戶資訊，以代表網路裝置執行註冊。                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | 設定 NDES 設定的屬性值。                                                                                                                                                                                                                                  |



 

 

 
