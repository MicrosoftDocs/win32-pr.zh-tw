---
description: CAMThread 類別是用來管理工作者執行緒的抽象類別。
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: 'CAMThread 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984031"
---
# <a name="camthread-class"></a><span data-ttu-id="4e582-103">CAMThread 類別</span><span class="sxs-lookup"><span data-stu-id="4e582-103">CAMThread class</span></span>

<span data-ttu-id="4e582-104">`CAMThread`類別是用來管理工作者執行緒的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="4e582-104">The `CAMThread` class is an abstract class for managing worker threads.</span></span>



| <span data-ttu-id="4e582-105">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="4e582-105">Protected Member Variables</span></span>                                 | <span data-ttu-id="4e582-106">Description</span><span class="sxs-lookup"><span data-stu-id="4e582-106">Description</span></span>                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="4e582-107">**m \_ hThread**</span><span class="sxs-lookup"><span data-stu-id="4e582-107">**m\_hThread**</span></span>](camthread-m-hthread.md)                  | <span data-ttu-id="4e582-108">執行緒的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4e582-108">Handle to the thread.</span></span>                                                        |
| <span data-ttu-id="4e582-109">Public 成員變數</span><span class="sxs-lookup"><span data-stu-id="4e582-109">Public Member Variables</span></span>                                    | <span data-ttu-id="4e582-110">Description</span><span class="sxs-lookup"><span data-stu-id="4e582-110">Description</span></span>                                                                  |
| [<span data-ttu-id="4e582-111">**m \_ AccessLock**</span><span class="sxs-lookup"><span data-stu-id="4e582-111">**m\_AccessLock**</span></span>](camthread-m-accesslock.md)            | <span data-ttu-id="4e582-112">防止其他執行緒存取執行緒的重要區段。</span><span class="sxs-lookup"><span data-stu-id="4e582-112">Critical section that locks the thread from being accessed by other threads.</span></span> |
| [<span data-ttu-id="4e582-113">**m \_ WorkerLock**</span><span class="sxs-lookup"><span data-stu-id="4e582-113">**m\_WorkerLock**</span></span>](camthread-m-workerlock.md)            | <span data-ttu-id="4e582-114">鎖定執行緒之間共用之資料的重要區段。</span><span class="sxs-lookup"><span data-stu-id="4e582-114">Critical section that locks data shared among threads.</span></span>                       |
| <span data-ttu-id="4e582-115">公用方法</span><span class="sxs-lookup"><span data-stu-id="4e582-115">Public Methods</span></span>                                             | <span data-ttu-id="4e582-116">Description</span><span class="sxs-lookup"><span data-stu-id="4e582-116">Description</span></span>                                                                  |
| [<span data-ttu-id="4e582-117">**CAMThread**</span><span class="sxs-lookup"><span data-stu-id="4e582-117">**CAMThread**</span></span>](camthread-camthread.md)                   | <span data-ttu-id="4e582-118">函式方法。</span><span class="sxs-lookup"><span data-stu-id="4e582-118">Constructor method.</span></span>                                                          |
| [<span data-ttu-id="4e582-119">**~ CAMThread**</span><span class="sxs-lookup"><span data-stu-id="4e582-119">**~ CAMThread**</span></span>](camthread--camthread.md)                | <span data-ttu-id="4e582-120">函式方法。</span><span class="sxs-lookup"><span data-stu-id="4e582-120">Destructor method.</span></span> <span data-ttu-id="4e582-121">虛擬。</span><span class="sxs-lookup"><span data-stu-id="4e582-121">Virtual.</span></span>                                                  |
| [<span data-ttu-id="4e582-122">**InitialThreadProc**</span><span class="sxs-lookup"><span data-stu-id="4e582-122">**InitialThreadProc**</span></span>](camthread-initialthreadproc.md)   | <span data-ttu-id="4e582-123">在建立執行緒時呼叫 ThreadProc 方法。</span><span class="sxs-lookup"><span data-stu-id="4e582-123">Calls the ThreadProc method when the thread is created.</span></span>                      |
| [<span data-ttu-id="4e582-124">**建立**</span><span class="sxs-lookup"><span data-stu-id="4e582-124">**Create**</span></span>](camthread-create.md)                         | <span data-ttu-id="4e582-125">建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="4e582-125">Creates the thread.</span></span>                                                          |
| [<span data-ttu-id="4e582-126">**CallWorker**</span><span class="sxs-lookup"><span data-stu-id="4e582-126">**CallWorker**</span></span>](camthread-callworker.md)                 | <span data-ttu-id="4e582-127">向執行緒發出要求的信號。</span><span class="sxs-lookup"><span data-stu-id="4e582-127">Signals the thread with a request.</span></span>                                           |
| [<span data-ttu-id="4e582-128">**關閉**</span><span class="sxs-lookup"><span data-stu-id="4e582-128">**Close**</span></span>](camthread-close.md)                           | <span data-ttu-id="4e582-129">等候執行緒結束，然後釋放其資源。</span><span class="sxs-lookup"><span data-stu-id="4e582-129">Waits for the thread to exit, then releases its resources.</span></span>                   |
| [<span data-ttu-id="4e582-130">**ThreadExists**</span><span class="sxs-lookup"><span data-stu-id="4e582-130">**ThreadExists**</span></span>](camthread-threadexists.md)             | <span data-ttu-id="4e582-131">查詢執行緒是否存在。</span><span class="sxs-lookup"><span data-stu-id="4e582-131">Queries whether the thread exists.</span></span>                                           |
| [<span data-ttu-id="4e582-132">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="4e582-132">**GetRequest**</span></span>](camthread-getrequest.md)                 | <span data-ttu-id="4e582-133">等候下一個要求。</span><span class="sxs-lookup"><span data-stu-id="4e582-133">Waits for the next request.</span></span>                                                  |
| [<span data-ttu-id="4e582-134">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="4e582-134">**CheckRequest**</span></span>](camthread-checkrequest.md)             | <span data-ttu-id="4e582-135">檢查是否有要求，而不封鎖。</span><span class="sxs-lookup"><span data-stu-id="4e582-135">Checks if there is a request, without blocking.</span></span>                              |
| [<span data-ttu-id="4e582-136">**回覆**</span><span class="sxs-lookup"><span data-stu-id="4e582-136">**Reply**</span></span>](camthread-reply.md)                           | <span data-ttu-id="4e582-137">回復要求。</span><span class="sxs-lookup"><span data-stu-id="4e582-137">Replies to a request.</span></span>                                                        |
| [<span data-ttu-id="4e582-138">**GetRequestHandle**</span><span class="sxs-lookup"><span data-stu-id="4e582-138">**GetRequestHandle**</span></span>](camthread-getrequesthandle.md)     | <span data-ttu-id="4e582-139">抓取 CallWorker 方法所發出之事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4e582-139">Retrieves a handle to the event signaled by the CallWorker method.</span></span>           |
| [<span data-ttu-id="4e582-140">**GetRequestParam**</span><span class="sxs-lookup"><span data-stu-id="4e582-140">**GetRequestParam**</span></span>](camthread-getrequestparam.md)       | <span data-ttu-id="4e582-141">捕獲最新的要求。</span><span class="sxs-lookup"><span data-stu-id="4e582-141">Retrieves the latest request.</span></span>                                                |
| [<span data-ttu-id="4e582-142">**CoInitializeHelper**</span><span class="sxs-lookup"><span data-stu-id="4e582-142">**CoInitializeHelper**</span></span>](camthread-coinitializehelper.md) | <span data-ttu-id="4e582-143">線上程的開頭呼叫 CoInitializeEx。</span><span class="sxs-lookup"><span data-stu-id="4e582-143">Calls CoInitializeEx at the start of the thread.</span></span>                             |
| <span data-ttu-id="4e582-144">純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="4e582-144">Pure Virtual Methods</span></span>                                       | <span data-ttu-id="4e582-145">Description</span><span class="sxs-lookup"><span data-stu-id="4e582-145">Description</span></span>                                                                  |
| [<span data-ttu-id="4e582-146">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="4e582-146">**ThreadProc**</span></span>](camthread-threadproc.md)                 | <span data-ttu-id="4e582-147">執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="4e582-147">Thread procedure.</span></span>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="4e582-148">備註</span><span class="sxs-lookup"><span data-stu-id="4e582-148">Remarks</span></span>

<span data-ttu-id="4e582-149">這個類別提供建立背景工作執行緒、將要求傳遞至執行緒，以及等待中的執行緒結束的方法。</span><span class="sxs-lookup"><span data-stu-id="4e582-149">This class provides methods for creating a worker thread, passing requests to the thread, and waiting for the thread to exit.</span></span> <span data-ttu-id="4e582-150">若要使用此類別，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="4e582-150">To use this class, do the following:</span></span>

-   <span data-ttu-id="4e582-151">從衍生類別 `CAMThread` ，並覆寫純虛擬方法 [**CAMThread：： ThreadProc**](camthread-threadproc.md)。</span><span class="sxs-lookup"><span data-stu-id="4e582-151">Derive a class from `CAMThread` and override the pure virtual method [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="4e582-152">這個方法是線上程開始時呼叫的執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="4e582-152">This method is the thread procedure that gets called at the start of the thread.</span></span>
-   <span data-ttu-id="4e582-153">在您的應用程式中，建立衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4e582-153">In your application, create an instance of your derived class.</span></span> <span data-ttu-id="4e582-154">建立物件並不會建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="4e582-154">Creating the object does not create the thread.</span></span> <span data-ttu-id="4e582-155">若要建立執行緒，請呼叫 [**CAMThread：： create**](camthread-create.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4e582-155">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>
-   <span data-ttu-id="4e582-156">若要將要求傳送至執行緒，請呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4e582-156">To send requests to the thread, call the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="4e582-157">這個方法會採用 DWORD 參數，其意義是由您的類別定義。</span><span class="sxs-lookup"><span data-stu-id="4e582-157">This method takes a DWORD parameter, whose meaning is defined by your class.</span></span> <span data-ttu-id="4e582-158">方法會封鎖，直到執行緒回應 (請參閱以下) 。</span><span class="sxs-lookup"><span data-stu-id="4e582-158">The method blocks until the thread responds (see below).</span></span>
-   <span data-ttu-id="4e582-159">在您的執行緒程式中，藉由呼叫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 或 [**CAMThread：： CheckRequest**](camthread-checkrequest.md)來回應要求。</span><span class="sxs-lookup"><span data-stu-id="4e582-159">In your thread procedure, respond to requests by calling either [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md).</span></span> <span data-ttu-id="4e582-160">GetRequest 方法會封鎖，直到另一個執行緒呼叫 CallWorker 為止。</span><span class="sxs-lookup"><span data-stu-id="4e582-160">The GetRequest method blocks until another thread calls CallWorker.</span></span> <span data-ttu-id="4e582-161">CheckRequest 方法為非封鎖，可讓執行緒在非同步工作時檢查是否有新的要求。</span><span class="sxs-lookup"><span data-stu-id="4e582-161">The CheckRequest method is non-blocking, which enables the thread to check for new requests while working asynchronously.</span></span>
-   <span data-ttu-id="4e582-162">當執行緒收到要求時，請呼叫 [**CAMThread：： Reply**](camthread-reply.md) 來解除封鎖呼叫執行緒。</span><span class="sxs-lookup"><span data-stu-id="4e582-162">When the thread receives a request, call [**CAMThread::Reply**](camthread-reply.md) to unblock the calling thread.</span></span> <span data-ttu-id="4e582-163">Reply 方法會採用 DWORD 參數，該參數會傳遞至呼叫的執行緒做為 CallWorker 的傳回值。</span><span class="sxs-lookup"><span data-stu-id="4e582-163">The Reply method takes a DWORD parameter, which is passed to the calling thread as the return value for CallWorker.</span></span>

<span data-ttu-id="4e582-164">當您完成執行緒時，請呼叫 [**CAMThread：： Close**](camthread-close.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4e582-164">When you are done with the thread, call the [**CAMThread::Close**](camthread-close.md) method.</span></span> <span data-ttu-id="4e582-165">這個方法會等候執行緒結束，然後關閉執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="4e582-165">This method waits for the thread to exit, and then closes the thread handle.</span></span> <span data-ttu-id="4e582-166">您的 ThreadProc 訊息必須保證會結束，或是回應 CallWorker 要求。</span><span class="sxs-lookup"><span data-stu-id="4e582-166">Your ThreadProc message must be guaranteed to exit, either on its own or in response to a CallWorker request.</span></span> <span data-ttu-id="4e582-167">「析構函數」方法也會呼叫 Close。</span><span class="sxs-lookup"><span data-stu-id="4e582-167">The destructor method also calls Close.</span></span>

<span data-ttu-id="4e582-168">下列範例說明這些步驟：</span><span class="sxs-lookup"><span data-stu-id="4e582-168">The following example illustrates these steps:</span></span>


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



<span data-ttu-id="4e582-169">在您的衍生類別中，您也可以定義成員函式，以驗證要 CallWorker 的參數。</span><span class="sxs-lookup"><span data-stu-id="4e582-169">In your derived class, you can also define member functions that validate the parameters to CallWorker.</span></span> <span data-ttu-id="4e582-170">下列範例顯示執行這項作業的典型方式：</span><span class="sxs-lookup"><span data-stu-id="4e582-170">The following example shows a typical way to do this:</span></span>


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



<span data-ttu-id="4e582-171">`CAMThread`類別提供兩個重要區段作為公用成員變數。</span><span class="sxs-lookup"><span data-stu-id="4e582-171">The `CAMThread` class provides two critical sections as public member variables.</span></span> <span data-ttu-id="4e582-172">用 `CAMThread::m_AccessLock` 來鎖定其他執行緒無法存取的執行緒。</span><span class="sxs-lookup"><span data-stu-id="4e582-172">Use `CAMThread::m_AccessLock` to lock the thread from being accessed by other threads.</span></span> <span data-ttu-id="4e582-173"> (例如，Create 和 CallWorker 方法會保存此鎖定，以序列化執行緒上的作業。 ) 使用 [**CAMThread：： m \_ WorkerLock**](camthread-m-workerlock.md) 來鎖定執行緒之間共用的資料。</span><span class="sxs-lookup"><span data-stu-id="4e582-173">(For example, the Create and CallWorker methods hold this lock, to serialize operations on the thread.) Use [**CAMThread::m\_WorkerLock**](camthread-m-workerlock.md) to lock data that is shared among threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e582-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e582-174">Requirements</span></span>



| <span data-ttu-id="4e582-175">需求</span><span class="sxs-lookup"><span data-stu-id="4e582-175">Requirement</span></span> | <span data-ttu-id="4e582-176">值</span><span class="sxs-lookup"><span data-stu-id="4e582-176">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e582-177">標頭</span><span class="sxs-lookup"><span data-stu-id="4e582-177">Header</span></span><br/>  | <dl> <span data-ttu-id="4e582-178"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4e582-178"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4e582-179">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e582-179">Library</span></span><br/> | <dl> <span data-ttu-id="4e582-180"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4e582-180"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




