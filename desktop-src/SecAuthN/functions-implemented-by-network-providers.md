---
description: 下列函式是由網路提供者 DLL 所執行，以與多個提供者路由器 (MPR) 進行通訊。
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: 網路提供者所執行的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945044"
---
# <a name="functions-implemented-by-network-providers"></a>網路提供者所執行的函式

下列函式是由網路提供者 DLL 所執行，以與 [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) (MPR) 進行通訊。 請注意，只有 [功能函數](capabilities-functions.md) 必須由網路提供者來執行。 其他類型的函式的執行是選擇性的，且取決於網路提供者的需求。



| 函數集                                                                                    | Description                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [功能功能](capabilities-functions.md)<br/>                                 | 允許呼叫者判斷網路提供者的功能。<br/>                                                                |
| [使用者名稱函式](user-name-functions.md)<br/>                                       | 提示網路提供者提供與連接相關聯的使用者名稱。<br/>                                                            |
| [裝置重新導向功能](device-redirecting-functions.md)<br/>                     | 允許網路提供者重新導向 Microsoft MS-DOS 作業系統上標準的裝置、磁碟機號和 LPT 埠。<br/> |
| [提供者特定的對話方塊函式](provider-specific-dialog-box-functions.md)<br/> | 允許網路提供者顯示或處理網路特定資訊。<br/>                                                            |
| [系統管理功能](administrative-functions.md)<br/>                             | 允許網路提供者顯示特殊的網路目錄或採取行動。<br/>                                                             |
| [列舉函數](enumeration-functions.md)<br/>                                   | 允許使用者流覽網路資源。<br/>                                                                                            |



 

如需有關如何建立和註冊網路提供者的詳細資訊，請參閱 [執行網路提供](implementing-a-network-provider.md) 者和註冊網路提供者 [和認證管理員](registering-network-providers-and-credential-managers.md)。

 

