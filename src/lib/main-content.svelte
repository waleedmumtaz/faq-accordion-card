<script>
  const setStyles = (id) => {
    faqs[id - 1].questionStyles =
      faqs[id - 1].questionStyles === '' ? 'font-bold' : ''
    faqs[id - 1].arrowStyles =
      faqs[id - 1].arrowStyles === '' ? 'rotate-180' : ''
  }

  let faqs = [
    {
      id: '1',
      question: 'How many team members can I invite?',
      answer:
        'You can invite up to 2 additional users on the Free plan. There is no limit on team members for the Premium plan.',
      questionStyles: '',
      arrowStyles: '',
    },
    {
      id: '2',
      question: 'What is the maximum file upload size?',
      answer:
        'No more than 2GB. All files in your account must fit your allotted storage space.',
      questionStyles: '',
      arrowStyles: '',
    },
    {
      id: '3',
      question: 'How do I reset my password?',
      answer:
        'Click “Forgot password” from the login page or “Change password” from your profile page. A reset link will be emailed to you.',
      questionStyles: '',
      arrowStyles: '',
    },
    {
      id: '4',
      question: 'Can I cancel my subscription?',
      answer:
        'Yes! Send us a message and we’ll process your request no questions asked.',
      questionStyles: '',
      arrowStyles: '',
    },
    {
      id: '5',
      question: 'Do you provide additional support?',
      answer:
        'Chat and email support is available 24/7. Phone lines are open during normal business hours.',
      questionStyles: '',
      arrowStyles: '',
    },
  ]
</script>

<main class="flex-1 flex flex-col justify-center pt-32">
  <div class="px-5 py-5 md:py-0 md:max-w-6xl md:mx-auto md:w-full relative">
    <img
      src="/assets/illustration-woman-online-mobile.svg"
      alt="woman online illustration"
      class="w-64 mx-auto md:hidden absolute -top-24 left-0 right-0 z-10"
    />
    <img
      src="/assets/bg-pattern-mobile.svg"
      alt="pattern"
      class="w-64 mx-auto md:hidden absolute top-5 left-0 right-0 z-10"
    />
    <div
      class="bg-white p-10 md:p-20 rounded-3xl shadow-lg relative overflow-hidden"
    >
      <div class="md:grid md:grid-cols-2 md:items-center">
        <div>
          <img
            src="/assets/illustration-woman-online-desktop.svg"
            alt="woman online illustration"
            class="max-w-md hidden md:block absolute top-16 -left-16"
          />
          <img
            src="/assets/illustration-box-desktop.svg"
            alt="box"
            class="hidden md:block absolute top-56 -left-10"
          />
          <img
            src="/assets/bg-pattern-desktop.svg"
            alt="pattern"
            class="hidden md:block absolute -top-72 -left-[36.5rem]"
          />
        </div>
        <div>
          <h1
            class="font-bold text-3xl text-center md:text-left pb-10 pt-28 md:pt-0"
          >
            FAQ
          </h1>
          {#each faqs as { id, question, answer, questionStyles, arrowStyles }}
            <details class="border-b-2 py-3">
              <summary
                on:click={() => setStyles(id)}
                class={`${questionStyles} list-none flex justify-between items-center hover:text-cstm-primary-text-soft-red cursor-pointer`}
              >
                {question}<span
                  ><img
                    src="/assets/icon-arrow-down.svg"
                    alt="down arrow"
                    class={`${arrowStyles} ml-3`}
                  /></span
                >
              </summary>
              <p
                class="pt-3 pr-3 cursor-text text-sm text-cstm-neutral-text-dark-grayish-blue"
              >
                {answer}
              </p>
            </details>
          {/each}
        </div>
      </div>
    </div>
  </div>
</main>
