---
description: 本主題說明您的應用程式如何指定 Tablet PC 剪取工具在捕捉應用程式時所應取得的 URL。
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Windows Vista 中的剪取工具支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850979"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Windows Vista 中的剪取工具支援

本主題說明您的應用程式如何指定 Tablet PC 剪取工具在捕捉應用程式時所應取得的 URL。

## <a name="specifying-the-url-via-registry-key"></a>透過登錄機碼指定 URL

剪取工具可讓使用者在螢幕上的任何物件 (螢幕擷取畫面) 捕捉剪取，然後加上批註、儲存或共用影像。 當資料儲存為 HTML 格式，或傳送至支援內嵌 HTML 的電子郵件客戶程式時，如果應用程式提供如何取得 URL 的相關資訊，剪取工具可以將 URL 加入至剪取。

剪取工具透過協助工具物件取得 URL。 應用程式應該在下列登錄機碼底下指定必要的資訊：

HKLM \\ Software \\ Microsoft \\ Windows \\ 平板 \\ 剪取工具 \\ LinkFingerprints，

而且應該建立一個子機碼，其名稱與應該從中取得連結的視窗類別相同。 視窗類別名稱應為應用程式的最上層視窗。

HKLM \\ Software \\ Microsoft \\ Windows \\ 平板 \\ 剪取工具 \\ LinkFingerprints\\<Window Class Name>

### <a name="window-class-key-details"></a>視窗類別索引鍵詳細資料

在視窗類別索引鍵下，應該設定適當的值，以指出剪取工具應該偵測正確的協助工具物件。



| 值                        | TYPE                  | 面具            | 儲存的資訊                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | REG \_ DWORD<br/> |                 | 指出下列哪些欄位要檢查<br/> |
| Name<br/>              | REG \_ SZ<br/>    | 0x02<br/> | 存取範圍名稱<br/>                               |
| Description<br/>       | REG \_ SZ<br/>    | 0x04<br/> | 協助工具描述<br/>                        |
| 角色<br/>              | REG \_ DWORD<br/> | 0x08<br/> | 協助工具角色<br/>                               |
| ParentName<br/>        | REG \_ SZ<br/>    | 0x10<br/> | 父系的協助工具名稱<br/>                     |
| ParentValue<br/>       | REG \_ SZ<br/>    | 0x20<br/> | 父系的協助工具值<br/>                    |
| ParentRole<br/>        | REG \_ DWORD<br/> | 0x40<br/> | 父系的協助工具角色<br/>                     |
| ParentDescription<br/> | REG \_ SZ<br/>    | 0x80<br/> | 父系的協助工具描述<br/>              |



 

此外，如果設定了遮罩位值0x1，則 URL 應該取自協助工具名稱;否則，應從存取範圍值取得 URL。

如果應用程式使用上述 REG SZ 值的當地語系化字串 \_ ，則應該使用下列格式，將字串提供為間接字串：

@filename資源

此字串會從名為的檔案中解壓縮，並使用資源值做為定位器。 如果資源值為零或大於零，則數位會成為二進位檔案中的字串索引。 如果數位為負數，則會變成 (識別碼) 的資源識別碼。

> [!Note]  
> 角色常數可以在 Windows SDK 的 oleacc 中找到。 描述的登錄值是 Windows Vista 特有的。

 

 

 




