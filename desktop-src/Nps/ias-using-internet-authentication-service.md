---
title: 使用 NPS 擴充功能
description: 網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- 網際網路驗證服務 IAS，工作
- 網際網路驗證服務 IAS，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104507844"
---
# <a name="using-nps-extensions"></a>使用 NPS 擴充功能

網際網路驗證服務 (IAS) 已重新命名 (NPS) 的網路原則伺服器。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

* * Windows Server 2008 R2 和 Windows Server 2008： * *

撥入和 MapName 範例會擴充 NPS 功能。



| 範例             | 描述                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 撥<br/>  | 此範例會執行 RADIUS 延伸模組 DLL，以檢查使用者的撥入位。<br/>                                                                                                              |
| MapName<br/> | 此範例延伸模組 DLL 會搜尋指定帳戶的所有受信任網域。 這可讓來自多個網域的使用者進行驗證，而不需要使用者提供其功能變數名稱。<br/> |



 

您可以在下列清單中找到 MapName 和撥入範例應用程式的原始程式碼。 *位置*，% 安裝路徑%，指定 x64 電腦的基底安裝目錄。 另請參閱 [Windows 軟體開發套件 (sdk) 以取得 Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)、Microsoft WINDOWS 軟體開發套件 (sdk) ，以及 [適用于 Windows Store 應用程式開發的下載](https://msdn.microsoft.com/windows/apps/br229516)。

<dl> <dt>

Windows 8 的 Windows SDK
</dt> <dd>

Windows Server 2012

下載連結： N/A

MapName：否

撥入：否

位置： N/A

</dd> <dt>

適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) 
</dt> <dd>

Windows Server 2008 R2

下載連結： <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName：是

撥入：否

位置：% 安裝路徑% \\ Microsoft sdk \\ Windows \\ 7.1 \\ 範例 \\ netds \\ ias

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

下載連結： <https://www.microsoft.com/download/details.aspx?id=5023>

MapName：是

撥入：否

位置：% 安裝路徑% \\ Microsoft sdk \\ Windows \\ 6.1 \\ 範例 \\ NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于開發人員的下載](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows 8 的 Windows SDK](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





