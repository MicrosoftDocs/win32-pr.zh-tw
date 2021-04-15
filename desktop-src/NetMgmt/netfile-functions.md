---
title: " (網路管理) 的 NetFile 函式"
description: 網路管理檔案功能提供一種方式來監視和關閉在伺服器上開啟的檔案、裝置和管道資源。 檔案功能如下所示。
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508260"
---
# <a name="netfile-functions-network-management"></a> (網路管理) 的 NetFile 函式

網路管理檔案功能提供一種方式來監視和關閉在伺服器上開啟的檔案、裝置和管道資源。 檔案功能如下所示。



| 函式                                | 描述                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | 強制關閉資源。                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | 傳回伺服器上開啟之檔案的相關資訊。                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | 傳回伺服器資源特定開啟的相關資訊。 |



 

當檔案無法以任何其他方式關閉時，請呼叫 [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) 函式。 因為 **NetFileClose** 不會在關閉檔案之前將用戶端系統上快取的資料寫入至檔案，所以應謹慎使用這個函數。

[**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)函數會傳回在伺服器上開啟之資源的相關資訊。 一個或多個應用程式可以開啟一或多次檔案。 每個檔案開啟都會唯一識別。 **NetFileEnum** 函式會傳回每個開啟檔案的專案。 [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo)函式會傳回一次開啟資源的相關資訊。

檔案資訊可在下列層級取得：

-   [**檔案 \_ 資訊 \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [**檔案 \_ 資訊 \_ 3**](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

不支援層級0和1。 層級2只會傳回在開啟時指派給資源的識別碼。 層級3會傳回識別碼、許可權、檔案鎖定，以及開啟資源之使用者的名稱。

如果您要針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以達到您可以藉由呼叫 [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) 和 [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) 函式達成的相同功能。 如需詳細資訊，請參閱 [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) 和 [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)。

 

 
